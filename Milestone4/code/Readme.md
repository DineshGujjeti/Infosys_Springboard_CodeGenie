# 🧞 CodeGenie

CodeGenie is a multi-user, AI-powered code generation and explanation tool. It is built entirely in Python using Streamlit, runs in a Google Colab environment, and is deployed via `ngrok`.

It features a secure authentication system, role-based access for admins, and a dynamic model-loading backend to stay within the memory limits of a free Colab GPU.


---

## ✨ Features

* **Secure Authentication:** Full user login, sign up, and password recovery (using a security question).
* **Role-Based Access:** The first user to register an account is automatically assigned the **Admin** role.
* **Dynamic Model Loading:** To conserve GPU VRAM, models are loaded dynamically. When you select a new model, the previous one is unloaded from memory, and the new one is loaded in its place.
* **On-Demand Pre-loading:** The model begins loading *as soon as you select it* from the dropdown, not when you click "Generate."
* **Code Generation:** Select from multiple models (Gemma, Phi-2, DeepSeek) to generate code snippets.
* **Code Explanation:** Get AI-powered, step-by-step explanations for your code.
* **AST Visualization:** Automatically generates and displays a visual Abstract Syntax Tree (AST) graph for any Python code you want to explain.
* **Code Complexity:** Calculates and logs the Cyclomatic Complexity (CC) for all generated Python code.
* **Full Admin Dashboard:** A private, multi-tab dashboard for the admin to:
    * View app metrics (Total Users, Total Queries, Avg. Latency).
    * See charts for language and model usage.
    * View all registered users, the full query history, and the full feedback log.
* **User Feedback System:** A complete 5-star rating and text comment form appears after every generation and explanation, which is then saved to the database.
* **User Profile:** A personal page where users can change their password and view their 10 most recent activities.

---

## 🛠️ Tech Stack

* **Framework:** [Streamlit](https://streamlit.io/)
* **Models:** [Hugging Face `transformers`](https://huggingface.co/docs/transformers/index)
* **GPU Optimization:** [NVIDIA `bitsandbytes`](https://github.com/TimDettmers/bitsandbytes) (for 4-bit quantization)
* **Database:** `sqlite3` (Python built-in)
* **Authentication:** `PyJWT` (for tokens), `bcrypt` (for hashing)
* **AST & Complexity:** `ast` (Python built-in), `graphviz`, `radon`
* **Data & Plotting:** `pandas`, `plotly-express`
* **Deployment:** Google Colab, `pyngrok`

---

## 🚀 How to Run (Google Colab)

This project is designed to be run entirely from a Google Colab notebook.

1.  **Open in Colab**
    Open the `.ipynb` notebook file in Google Colab.

2.  **Set Runtime to GPU**
    * Go to **Runtime** -> **Change runtime type**.
    * Select **T4 GPU** from the "Hardware accelerator" dropdown. This is required to run the models.

3.  **Add Colab Secrets**
    * In the Colab sidebar, click the **🔑 (key)** icon to open the Secrets Manager.
    * Add the following three secrets. The app will not run without them.
    * `HF_TOKEN`: Your Hugging Face **read** token. You *must* go to the [Gemma-2B-IT model card](https://huggingface.co/google/gemma-2b-it) and accept the license terms first, or the app will fail to load the model.
    * `JWT_SECRET_KEY`: A long, random string you create (e.g., from a password generator) used to sign user tokens.
    * `NGROK_TOKEN`: Your auth token from your [ngrok Dashboard](https://dashboard.ngrok.com/get-started/your-authtoken).

4.  **Run the Notebook Cells**
    Run the cells in the notebook in order:
    1.  **Cell 1: Install Dependencies:** This will install all required Python packages.
    2.  **Cell 2: Write app.py:** This will take the main application code and write it to a file named `app.py` in your Colab environment.
    3.  **Cell 3: Launch the App:** This will start the Streamlit server in the background and then use `ngrok` to create a public URL for you.

5.  **Access Your App**
    The final cell will output a public `ngrok` URL (it looks like `https://<some-name>.ngrok-free.dev`). Click this link to open and use your live application.

---

## ℹ️ Usage Notes

* **First User is Admin:** The very first account you register will be the admin.
* **Model Loading Time:** When you select a model from the dropdown for the first time (e.g., "Gemma-2B-IT"), the app will pause to download and load it. This is a one-time wait per model and can take **5-10 minutes** on a free Colab GPU.
* **Generation Time:** After a model is loaded, "thinking" (inference) time can still take 30-60 seconds.
* **Memory Crashes:** The free T4 GPU has limited memory. This app uses 4-bit quantization and dynamic swapping to save memory, but loading large models like Gemma or Phi-2 can still sometimes cause the app to crash (you will see an `ngrok` error page). If this happens:
    1.  **Restart the runtime** in Colab (Runtime -> Restart runtime...).
    2.  Re-run all three cells.
    3.  Try sticking to the smallest model, **DeepSeek-Coder-1.3B**, which is the most stable.
