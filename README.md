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

**CodeGenie** is an AI assistant designed to help developers, students, and professionals understand and generate code with clarity. Unlike standard assistants that give generic output, CodeGenie uses structural analysis and language-specific models to produce explanations that highlight logic, flow, and purpose.

It leverages:

- **AST-based Python explanation**
- **Transformer models for JS & SQL**
- **Secure user authentication (JWT + OTP)**
- **4-bit quantized models for efficiency**
- **Streamlit-based interactive UI**
- **Admin dashboard with analytics**

It is built for:

- Students learning code fundamentals  
- Developers onboarding to new codebases  
- Engineers maintaining complex logic  
- Trainers teaching real-world examples  
- Teams tracking AI usage with analytics  

---

# 🎯 Problem Statement & Motivation

When developers ask AI to explain or generate code, the result is often:

- Too generic  
- Technically correct but contextually wrong  
- Missing project-specific logic  
- Detached from actual architecture  
- Poorly aligned with the existing code style  

This is frustrating — especially for beginners or teams working with unfamiliar code.

### CodeGenie aims to change that by answering one question:

> **“What if AI could read your entire codebase before answering?”**

With RAG, vector search, AST parsing, and multi-model support, CodeGenie brings project-level intelligence into explanations, giving users:

- Accurate code explanations grounded in real project files  
- Cleaner and context-aware code generation  
- Better clarity and faster comprehension  
- Tools to learn how pieces of code connect  
- Secure and trackable usage with authentication & history  

---

# 🚀 Key Features

## 👤 User Capabilities


| Feature | Description |
|--------|-------------|
| 🔐 **Secure Authentication** | JWT login, refresh tokens, OTP password recovery |
| 🧠 **AST-Based Python Analysis** | Structural understanding of Python classes, functions, and flow |
| ✍️ **Text → Code Generation** | Generate Python/JS/SQL code from natural language |
| 🔄 **Mode Toggle** | Switch between code generation and explanation |
| 🌐 **Multi-Language Support** | Python, JavaScript, SQL |
| ⭐ **Feedback System** | Rate outputs and leave comments |
| 🕘 **History Log** | Archive of all queries, results, timestamps, and languages |
| 🔧 **Profile Management** | Update password and user preferences |

---

## 🛠 Admin Features

- Manage roles and control admin access
- Inspect user activity summaries
- View trending prompts & common queries
- Analyze code generation vs explanation usage
- Monitor language popularity
- Explore feedback statistics (ratings, comments, word clouds)
- Global search through users, queries, and explanations
- Evaluate model quality metrics and system performance

---

# 🧩 Architecture

A high-level overview:

- **Frontend (Streamlit)**  
  Clean UI for generating/explaining code, browsing history, and admin dashboards.

- **Backend (FastAPI)**  
  Handles authentication, history logging, model inference and admin APIs. 

- **AST Engine for Python**  
  Extracts structure, nodes, functions, classes to enhance explanations.
  
- **Models**  
  Multi-language support via transformer-based models.
  
 **SQLite Database**  
  Stores users, history, feedback, and admin data.
  
- **4-bit Quantization**  
  Models run efficiently on low-memory machines & Google Colab.

- **System Architecture**
- <img width="1871" height="598" alt="image" src="https://github.com/user-attachments/assets/3cf20a45-f609-4c9a-ac7a-5483c1fb89f6" />


-**ER Diagram**
-<img width="669" height="895" alt="image" src="https://github.com/user-attachments/assets/2370eebf-47c6-498b-ab68-2302e7d6583d" />

---

# 🛠 Tech Stack

| Layer | Technologies |
|-------|-------------|
| Frontend | Streamlit |
| Backend | FastAPI+Python |
| Models | HuggingFace Transformers |
| Parsing | Python AST |
| Database | SQLite |
| Auth | JWT + bcrypt |
| Email OTP | Gmail SMTP |
| Deployment | Docker |
| Optimization | 4-bit quantization |

---

# 🤖 Models Used

| Model | Purpose |
|-------|---------|
| **Phi / Gemma** | Python code explanation |
| **CodeBERT** | JS/SQL analysis |
| **CodeLlama** | Code generation & refinement |
| **DeepSeek-Coder** | Multi-language generation |
| **StarCoder2** | Pattern-aware rewriting |
| **AST Parsing** | Structural Python understanding |

---

# 📂 Project Structure

```bash
CodeGenie/
│
├── app.py                   # Streamlit UI
│
├── backend/
│   ├── auth.py              # JWT auth + role mgmt + OTP
│   ├── generator.py         # Code generation engine
│   ├── explainer.py         # RAG + AST code explanation
│   ├── rag_core.py          # Retrieval logic, embeddings, vector DB
│   ├── ast_engine.py        # Python AST parser
│   ├── history.py           # Query logging
│   ├── feedback.py          # Ratings + analytics
│   ├── admin.py             # Admin-only APIs
│   └── models.py            # SQLite models
│
├── requirements.txt
├── Dockerfile
├── .env.example
│
└── docs/
    ├── architecture.png
    ├── flow_diagram.png
    └── screenshots/
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

1. **Login or Sign Up**  
   Create an account or log in using your existing credentials.

2. **Choose a Mode**
   - **Generate Code** — Convert natural language into executable code  
   - **Explain Code** — Understand any snippet with RAG + AST assistance

3. **Pick a Language**
   - Python  
   - JavaScript  
   - SQL  

4. **Submit Your Input**
   - Paste a code snippet for explanation  
   - OR write an instruction for code generation  

5. **View Results**
   - Get a structured explanation with context from the entire codebase  
   - OR receive clean, runnable, and well-structured generated code  

6. **Provide Feedback**
   - Rate the result  
   - Add optional comments to help improve quality  

7. **Access History**
   - Browse all your past queries  
   - Revisit explanations and generated code  
   - Track timestamps, languages, and modes  
   - Continue learning at your own pace  

---

# 🛡 Admin Controls

Admins have access to additional management tools:

- **Manage User Roles**  
  Promote/demote users, control admin access (max 2 admins)

- **Track System-Wide Analytics**  
  Understand how users interact with the platform

- **Explore Trending Queries**  
  Identify most common prompts and code patterns

- **View Feedback Quality**  
  Analyze ratings and recurring user concerns

- **Monitor Model & System Stats**  
  Evaluate performance, usage frequency, and error trends  


---

# 📊 History & Analytics

### 🔍 What Gets Logged

Every user action (based on configuration) is captured with:

- Code snippet / prompt  
- AI-generated output  
- User identity  
- Programming language  
- Mode (Generation / Explanation)  
- Timestamp  
- Ratings & feedback  

### 📈 What Admins Can Visualize

The Admin Dashboard provides insights such as:

- Daily/weekly usage trend charts  
- Model usage heatmaps  
- Feedback-driven word clouds  
- Language distribution & popularity  
- Engagement metrics  


---

# 📸 Screenshots

_Actual UI screenshots will be added soon._

Suggested screenshots to include:

- Login & Signup  
- Main Dashboard  
- Code Generation Module  
- Code Explanation Module  
- Admin Analytics Dashboard  
- History & Logs View  


---

# 🧭 Roadmap

Future enhancements planned:

- [ ] Auto-index GitHub repositories directly  
- [ ] VS Code extension for real-time integration  
- [ ] Interactive Visual AST Explorer  
- [ ] Export explanations as PDF/Markdown  
- [ ] Project dependency & path visualizer  
- [ ] Custom fine-tuning for explanation-focused models  


---

# 👥 Team

| Name | Role | Responsibilities |
|------|------|------------------|
| Add Name | ML Engineer | RAG pipeline, model integration, quantization |
| Add Name | Backend Developer | APIs, database, auth, OTP system |
| Add Name | Frontend Developer | Streamlit UI & user experience |
| Add Name | Documentation Lead | README, architecture diagrams |
| Add Name | Lead | PPTs |


---

# 📜 License

**MIT License** — Free to use, modify, and distribute with attribution.


---

Made with ⚡ passion, 🧠 curiosity, and a commitment to helping developers truly understand their code.

