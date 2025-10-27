# 🧞 CodeGenie: AI Code Generator and Explainer

CodeGenie is a full-stack web application designed to empower developers and students. It provides secure user authentication while hosting large language models (LLMs) locally on a Google Colab GPU to generate and explain code efficiently, complete with visual tools like the Abstract Syntax Tree (AST) visualizer.

---

## ✨ Features

* **AI Code Generation:** Generates code snippets from natural language prompts using large, locally-loaded Hugging Face models (Gemma, DeepSeek-Coder, Phi-2).
* **Code Explanation:** Provides step-by-step explanations for code in multiple languages (Python, JS, SQL) using LLMs.
* **Python AST Visualization:** Visually represents the structure of valid Python code using `graphviz`.
* **Secure Authentication:** Includes user sign-up, login, password reset, and an Admin Panel, all secured with `sqlite3`, `bcrypt`, and `PyJWT`.
* **Efficient GPU Usage:** Utilizes Streamlit's `@st.cache_resource` and 4-bit quantization (`bitsandbytes`) to load models only once and minimize VRAM usage.
* **Public Access:** Deployed seamlessly via Google Colab and exposed over a public URL using `pyngrok`.

---

## 🚀 Quick Start (Running in Google Colab)

Follow these steps within your Colab notebook to get CodeGenie running.

### Prerequisites

1.  **Google Colab Pro/Tiers:** While possible on the free tier, having a dedicated GPU (T4, V100, etc.) is highly recommended.
2.  **Hugging Face (HF) Token:** A **Read Token** is required to download models like Gemma.
3.  **ngrok Authtoken:** Required to create the public URL.

### Installation & Deployment Steps

1.  **Set Secrets and Install Dependencies:**
    * Open your Colab notebook.
    * In the first code cell, ensure your `HF_TOKEN_VALUE`, `JWT_SECRET_VALUE`, and `NGROK_TOKEN_VALUE` are correctly set.
    * Ensure your installation cell includes the critical package `bitsandbytes`:

        ```bash
        !pip install streamlit pyngrok PyJWT bcrypt requests graphviz ipywidgets pandas matplotlib seaborn radon
        !pip install bitsandbytes # Crucial for 4-bit quantization
        !pip install transformers accelerate
        ```

2.  **Write and Save `app.py`:**
    * Run the cell containing the `%%writefile app.py` command. This updates the Streamlit application logic with the corrected model caching and authentication.

3.  **Deploy the Application:**
    * Run the final deployment cell (the one containing `ngrok.connect(8501)`).
    * Wait for the output to display the public URL:

        ```
        Your CodeGenie app is live at:
        NgrokTunnel: "[https://your-unique-subdomain.ngrok-free.dev](https://your-unique-subdomain.ngrok-free.dev)" -> "http://localhost:8501"
        ```

4.  **Access the App:** Click the generated public ngrok URL.

---

## 💡 Key Usage Notes

### First Login & Setup

* **Initial User:** The very first user to sign up will automatically be assigned the **Admin** role.
* **Model Loading:** After logging in, the first time you visit the **Code Generator** or **Code Explainer** page, the model will start downloading and loading onto the GPU (this can take 5-15 minutes). **Wait for the "Model loaded successfully!" message** before attempting to generate code.

### Troubleshooting

| Issue | Cause | Solution |
| :--- | :--- | :--- |
| **Model Not Found (404)** | Using the wrong model slugs for external APIs (old issue). | **Fix:** Ensure all model IDs in `MODELS` are correct Hugging Face repository names (e.g., `google/gemma-2b-it`). |
| **Script execution error (Indentation)** | Invalid spacing/characters in `app.py`. | **Fix:** Ensure all code blocks use consistent indentation (4 spaces). |
| **Stuck on "Thinking..."** | The model is loading in the background. | **Fix:** Wait for the "Model loaded successfully!" message before clicking generate. |
| **`PackageNotFoundError: bitsandbytes`** | The required library for GPU optimization is missing. | **Fix:** Ensure `!pip install bitsandbytes` is run successfully in the dependency cell. |

---

## 📜 Technical Stack

* **Web Framework:** Streamlit
* **LLMs/AI:** Hugging Face Transformers, AutoModelForCausalLM, AutoTokenizer
* **GPU Optimization:** PyTorch, `bitsandbytes` (4-bit quantization)
* **Authentication:** SQLite (Database), `bcrypt` (Hashing), `PyJWT` (Tokens)
* **Tunneling/Deployment:** `pyngrok`
* **Visualization:** `graphviz`
