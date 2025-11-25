# 🧠 CodeGenie  
_Futuristic AI Code Explainer & Intelligent Code Generation Platform_  
Helping developers understand code the way humans do — with clarity, structure, and context.

---

## 🔗 Quick Links

| Category            | Link          |
|--------------------|---------------|
| 🎥 Demo Video      | Coming Soon   |
| 🐳 Docker Support | Yes           |
| 💡 Supported Languages | Python · JavaScript · SQL |

---

## 🌟 Introduction

Modern AI code assistants are powerful, but they all share one fundamental flaw:  
they don’t understand your codebase.

They know how programming works in general, but not how your modules connect, how your functions are designed, or why your project is structured the way it is. As a result, they often hallucinate explanations, make incorrect assumptions, and miss the deeper intent behind your code. Developers end up with answers that look convincing but aren’t aligned with the actual logic or architecture of the project.

CodeGenie was created to solve this gap.

Instead of giving shallow or generic explanations, CodeGenie focuses on delivering *structured, meaningful, and context-conscious insights* into your code. Through AST-powered Python analysis, language-specific models, and carefully engineered explanation logic, it breaks code down the same way an experienced engineer would — into purpose, flow, structure, and reasoning.

The result?  
Explanations that feel like they came from someone who actually understands how code works, why it was written that way, and how it fits into the bigger picture.

With CodeGenie, you can:

- Understand complex or legacy code with clarity  
- Generate clean, reliable code across Python, JavaScript, and SQL  
- Learn programming concepts through intuitive breakdowns  
- Track your interactions and revisit past explanations  
- Manage everything smoothly through a minimal, polished, interactive UI  

Initially built during an Infosys Springboard Internship, CodeGenie has evolved into a refined AI-driven coding assistant grounded in real-world engineering practices, strong model integration, and a user experience shaped for both learning and productivity.


---

## 📌 Table of Contents

- [About the Project](#-about-the-project)  
- [Problem Statement & Motivation](#-problem-statement--motivation)  
- [Key Features](#-key-features)  
- [Architecture](#-architecture)  
- [Tech Stack](#-tech-stack)  
- [Models Used](#-models-used)  
- [Project Structure](#-project-structure)  
- [Installation & Setup](-#installation--setup)
- [Usage Guide](#-usage-guide)  
- [Admin Controls](#-admin-controls)  
- [History & Analytics](#-history--analytics)  
- [Screenshots](#-screenshots)  
- [Roadmap](#-roadmap)  
- [Team](#-team)  
- [License](#-license)

---

# 📖 About the Project

**CodeGenie** is an AI-powered coding assistant built to make code feel less like a puzzle and more like a story you can actually follow.

Most tools can tell you what a line of code *does* in isolation. CodeGenie goes further — it focuses on **structure, intent, and learning**, breaking down snippets into human-readable logic, complexity, and flow. It also helps you generate new code that is clean, readable, and ready to run.

Originally developed as part of the **Infosys Springboard Internship**, CodeGenie has grown into a compact but powerful platform for:

- Students trying to understand how real code works  
- Developers onboarding into unfamiliar projects  
- Trainers and educators who need explainable examples  
- Engineers who want quick, reliable code generation and explanation in one place  

At its core, CodeGenie blends:

- **AST-based Python analysis** for deep structural understanding  
- **Specialized models** for Python, JavaScript, and SQL  
- **Secure authentication & role-based access**  
- **Streamlit UI** for a smooth, interactive experience  
- **Analytics & feedback loops** to track quality and usage over time  
- **4-bit model quantization** for efficient deployment on limited hardware / Google Colab  

---

# 🎯 Problem Statement & Motivation

Modern AI assistants are impressive — but they often miss the point when it comes to *your* code:

- They explain code generically without understanding structure.
- They ignore how functions, classes, and modules relate to each other.
- They may hallucinate details or oversimplify complex logic.
- Beginners get overwhelmed; experienced devs get frustrated.

**CodeGenie was created to close this gap.**

Instead of acting like a generic chatbot, CodeGenie behaves more like a patient teammate:

- It breaks code into **logical blocks**, **control flow**, and **complexity**.  
- It uses **AST (Abstract Syntax Tree)** parsing for Python to understand code structure rather than just surface tokens.  
- It supports **mode switching** — explain existing code or generate new code from natural language.  
- It tracks **history, feedback, and language usage**, turning every interaction into a learning signal.

The result is an assistant that feels more intentional, more transparent, and more educational.

---

# 🚀 Key Features

## 👤 User Capabilities


| Module                    | Description |
|---------------------------|-------------|
| 🔐 **Secure Authentication** | JWT-based login, refresh tokens, and protected routes |
| 👥 **User Roles & Profiles** | User/Admin roles with basic profile & preference management |
| ✍️ **Text → Code Generator** | Turn plain English into runnable **Python / JavaScript / SQL** code |
| 🧩 **Code → Explanation** | Explain code step-by-step with logic, structure, and complexity |
| 🧠 **AST-Powered Python Insights** | Python code is parsed structurally for richer explanations |
| 🔀 **Mode Toggle** | Seamlessly switch between **Generate** and **Explain** modes in the UI |
| ⭐ **Ratings & Feedback** | Feedback form on every output to rate quality and add comments |
| 🕘 **User History & Logs** | Track all queries, outputs, timestamps, languages, and modes |
| 🔏 **Profile & Password Management** | Update profile; change password with re-authentication |
| 📩 **Forgot Password (Gmail OTP)** | Secure OTP-based recovery using Gmail SMTP |
| 🧮 **4-bit Quantization Support** | Memory-optimized model loading (bits-and-bytes style workflow) |

---

## 🛠 Admin Features

Admin users get access to additional tools and dashboards:

- Manage user roles and permissions (with a cap on number of admins).  
- View **trending queries** and most active languages.  
- Monitor **model usage** and mode distribution (generation vs explanation).  
- Inspect **feedback statistics** — average ratings, common comments.  
- Access **growth and usage charts** over time.  
- Review **history logs** for debugging and quality control.  
- Use an **Admin Panel** UI to navigate analytics and controls in one place.

---

# 🧩 Architecture

CodeGenie is designed as a modular, secure, and analytics-aware platform.

- **Frontend:**  
  - Built with **Streamlit** for rapid, interactive UI.  
  - Allows users to log in, generate/explain code, view history, and submit feedback.

- **Backend & Services:**  
  - Core logic written in **Python**.  
  - Authentication handled with **JWT + bcrypt**.  
  - Email / OTP services via **Gmail SMTP**.  
  - SQLite database for users, history, and feedback.  

- **AI & Processing Layer:**  
  - Model wrappers for Python, JS, and SQL.  
  - **AST parsing** for Python explanation.  
  - 4-bit quantized models for memory-efficient execution.  
  - Separate flows for **code generation** and **code explanation**.

- **Security & Isolation:**  
  - Token-based user isolation.  
  - Minimal exposure of sensitive data.  
  - Proper separation between user routes and admin tools.


- **System Architecture:**
  
- <img width="1871" height="598" alt="image" src="https://github.com/user-attachments/assets/3cf20a45-f609-4c9a-ac7a-5483c1fb89f6" />

- **ER Diagram**

- <img width="669" height="895" alt="image" src="https://github.com/user-attachments/assets/2370eebf-47c6-498b-ab68-2302e7d6583d" />

---

# 🛠 Tech Stack

| Component      | Technology |
|----------------|-----------|
| Frontend       | Streamlit |
| Backend        | Python |
| AI & NLP       | Hugging Face Transformers |
| Models         | CodeBERT · Phi / Gemma · CodeLlama · DeepSeek-Coder · StarCoder2 |
| Parsing        | Python `ast` module |
| Database       | MongoDB |
| Authentication | JWT + bcrypt |
| Email          | Gmail SMTP (OTP delivery) |
| Deployment     | Docker, Google Colab-friendly setup |
| Optimization   | 4-bit model quantization for reduced VRAM usage |

---

# 🤖 Models Used

| Model / Tool      | Use Case                          | Notes |
|-------------------|-----------------------------------|-------|
| **Phi / Gemma**   | Python explanation & generation   | Compact, instruction-tuned models for reasoning about Python |
| **CodeBERT**      | JS & SQL understanding            | Token-level representation and embedding of code |
| **CodeLlama**     | General code generation           | Handles multi-language prompts and refinement |
| **DeepSeek-Coder**| Multi-language code suggestions   | Efficient pattern learning for common coding tasks |
| **StarCoder2**    | Code rewriting & improvements     | Good for refactoring and completion-style tasks |
| **AST Parsing**   | Python explanation engine         | Converts code into an Abstract Syntax Tree for structural insight |
| **Custom Tokenizers / Pipelines** | JS & SQL explanations | Tailored token processing for non-Python languages |

(Exact models and sizes can be tuned based on your hardware and use case.)

---

# 📂 Project Structure

```bash
CodeGenie/
│
├── app.py                  # Main Streamlit UI entry point
│
├── backend/
│   ├── auth.py             # JWT auth, signup/login, role management
│   ├── generator.py        # Text-to-code generation logic
│   ├── explainer.py        # Code explanation (Python AST + models)
│   ├── models.py           # SQLite ORM / DB helpers
│   ├── history.py          # User history and logging utilities
│   ├── feedback.py         # Feedback storage & analytics helpers
│   ├── admin.py            # Admin-specific routes and queries
│   └── utils.py            # Shared helpers (email, OTP, etc.)
│
├── notebooks/
│   └── CodeGenie_colab.ipynb   # Colab notebook version (optional)
│
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container setup
├── .env.example            # Environment variable template
│
└── docs/
    ├── architecture.png    # System architecture diagram
    ├── er_diagram.png      # ER / database schema
    └── screenshots/        # UI screenshots
```

---

## ❄️ Installation & Setup

### **Prerequisites**
- Python 3.10+
- Git
- (Optional) Docker

---

### **Clone & Install**
```bash
git clone <repo-link>
cd CodeGenie
pip install -r requirements.txt
JWT_SECRET_KEY=your_key_here
SMTP_EMAIL=your_mail_here
SMTP_PASSWORD=your_app_pass_here
streamlit run app.py
```

# 📝 Usage Guide

1. **Sign Up or Log In**
   - Create a new account or log in with your existing credentials.
   - Authentication is handled securely using JWT.

2. **Choose What You Want To Do**
   - **Generate Code** – turn natural language instructions into runnable code.
   - **Explain Code** – paste a code snippet and get a structured explanation.

3. **Pick a Language**
   - Python  
   - JavaScript  
   - SQL  

4. **Provide Input**
   - For **Generate Code**: type your problem statement or description of what you want.
   - For **Explain Code**: paste the code snippet you want clarified.

5. **View the Result**
   - For explanations: see logic breakdown, step-by-step flow, and (where applicable) complexity notes.
   - For generation: get clean, formatted code tailored to the selected language.

6. **Interact With the Output**
   - Copy the generated code to your editor.
   - Re-run or refine your query with more details.
   - Toggle between **Generation** and **Explanation** modes directly from the UI.

7. **Give Feedback**
   - Rate the response quality (e.g., ⭐ 1–5).
   - Optionally add a short text comment about what worked and what didn’t.

8. **Explore Your History**
   - Open the **History** section to:
     - Revisit past prompts and outputs.
     - Filter by language, mode (generation/explanation), or date.
     - Re-run older queries with updated models.

---

# 🛡 Admin Controls

Admin users get access to an extended, role-based control panel:

- **User & Role Management**
  - View the list of all registered users.
  - Promote or demote users between regular and admin roles (with a cap on total admins).
  - Lock or unlock accounts if misuse is detected.

- **System Usage Overview**
  - Monitor how often each module is used (generation vs explanation).
  - See active users, returning users, and new signups over time.

- **Language & Feature Analytics**
  - Track which languages (Python / JS / SQL) are used most.
  - Inspect the distribution of queries across code generation and code explanation.

- **Feedback & Quality Monitoring**
  - View average ratings over time.
  - Drill into low-rated responses to understand pain points.
  - Browse feedback comments to guide improvements.

- **Audit & Logs**
  - Access summarized logs of user actions (without exposing sensitive content).
  - Use this data for debugging, moderation, and system tuning.

---

# 📊 History & Analytics

CodeGenie keeps structured logs so both users and admins can understand how the app is being used.

### 🔐 What Gets Stored

Each interaction can include:

- User identifier
- Code snippet or prompt (sanitized/limited as configured)
- Model output (generated code or explanation)
- Selected language (Python / JS / SQL)
- Mode (Code Generation / Code Explanation)
- Timestamp of the request
- Feedback rating and optional text comment

### 📈 What You Can See

**For Users:**

- A personal **History** view that allows you to:
  - Scroll through past sessions.
  - Re-open previous prompts.
  - Copy old outputs.
  - Compare how explanations or generations improve over time.

**For Admins (Analytics Dashboard):**

- **Trend charts**
  - Daily/weekly request counts.
  - Growth of active users.
- **Language usage stats**
  - Popularity of Python vs JS vs SQL.
- **Feature usage**
  - How often “Generate” vs “Explain” is used.
- **Feedback insights**
  - Average rating per time window.
  - Word cloud or summary of common feedback terms.
- **System health indicators**
  - Error rates, failed requests, or timeout counts (if tracked).

These insights help guide improvements to the models, UI, and user experience.

---

# 📸 Screenshots

_Actual UI screenshots will be added soon._


- Login & Signup  
- Main Dashboard  
- Code Generation Module  
- Code Explanation Module  
- Admin Analytics Dashboard  
- History & Logs View  


---

# 🧭 Roadmap

Planned and potential future enhancements for CodeGenie:

- [ ] **Deeper IDE Integration**
  - VS Code / JetBrains plugin for inline explain & generate actions.
- [ ] **GitHub / Repo-Aware Context**
  - Smarter understanding of project structure and relationships between files.
- [ ] **Visual AST Explorer**
  - Interactive tree view for Python code showing functions, classes, and control flow.
- [ ] **Export & Share**
  - Export explanations as PDF or Markdown for documentation or teaching material.
- [ ] **Project Flow & Dependency Maps**
  - Visual diagrams that show how modules, functions, and files connect.
- [ ] **Advanced Admin Analytics**
  - More detailed dashboards for performance, latency, and per-model breakdowns.
- [ ] **Custom Model Fine-Tuning**
  - Allow domain or organization-specific tuning for better explanations.
- [ ] **More Language Support**
  - Add support for additional languages beyond Python, JavaScript, and SQL.

> This roadmap is aspirational and may evolve as feedback is received and the project grows.

# 👥 Team

| Name | Role | Responsibilities |
|------|------|------------------|
| Add Name | ML Engineer | model integration, quantization |
| Add Name | Backend Developer | APIs, database, auth, OTP system |
| Add Name | Frontend Developer | Streamlit UI & user experience |
| Add Name | Documentation Lead | README, architecture diagrams |
| Add Name | Lead | PPTs |


---

# 📜 License

**MIT License** — Free to use, modify, and distribute with attribution.


---

Made with ⚡ passion, 🧠 curiosity, and a commitment to helping developers truly understand their code.

