<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/051c4dd1-868f-412a-814f-d907e7122ea3" />

# 🧞‍♂️ CodeGenie
### AI Explainer and Code Generation Platform

> **Convert ideas into clean code and code into clear understanding.**

[![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Backend-Python-3776AB?style=for-the-badge&logo=python)](https://www.python.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB_Atlas-47A248?style=for-the-badge&logo=mongodb)](https://www.mongodb.com/)
[![Hugging Face](https://img.shields.io/badge/Models-Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface)](https://huggingface.co/)

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

**CodeGenie** is an AI-powered software development assistant designed to help beginners and engineers write efficient code and understand complex programming concepts.

**Problem Statement:**
Programming can be hard for beginners because understanding logic takes time and writing optimized code requires expertise.

**CodeGenie removes these barriers by:**
* Generating runnable code from plain English prompts.
* Explaining code logic using AST parsing (Python) and AI (other languages).
* Providing an interactive chat interface for general programming queries.

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

### User Capabilities
| Module | Description | Status |
| :--- | :--- | :--- |
| **Secure Authentication** | JSON Web Token(JWT) login, Google OAuth integration, and OTP-based password recovery via Email. | ☑ |
| **Code Generator** | Converts natural language prompts into Python, JavaScript, SQL, C++, etc. | ☑ |
| **Code Explainer** | Parses Python using AST for structural breakdown and AI for logic explanation. | ☑ |
| **AI Chatbot** | Context-aware general coding assistant (powered by Phi-2). | ☑ |
| **Workspace History** | Automatically saves all generations and explanations to MongoDB. | ☑ |
| **File Management** | Upload and manage coding files (Auto-cleanup for old files). | ☑ |

### Admin Features
* **User Management:** View, suspend, delete, or promote users to Admin roles.
* **Request Handling:** Approve or reject user requests for elevated privileges.
* **Analytics Dashboard:**
    * User signup trends.
    * Daily login activity.
    * Model popularity (Pie charts).
    * Activity heatmaps (Day vs. Hour).
* **Data Export:** Download Users, Logs, and History as CSV or PDF.

---

# 🧩 Architecture

The application follows a modular architecture powered by Streamlit for the frontend and Python for backend logic, connecting to MongoDB Atlas for persistence.

* **Frontend:** Streamlit (Single Page Application).
* **Authentication:** Dual-layer auth using Local (Bcrypt+JSON Web Token(JWT)) and Google OAuth2.
* **Model Layer:** Local execution of Hugging Face Transformers (`pipeline`).
* **Database:** Cloud-hosted MongoDB Atlas.
- **System Architecture:**
  
- <img width="1284" height="961" alt="image" src="https://github.com/user-attachments/assets/0a476a22-1942-46c3-9df7-8f22a1124236" />


- **ER Diagram**

- <img width="1409" height="729" alt="image" src="https://github.com/user-attachments/assets/223af2e6-9853-48cc-b262-757a20066cd1" />


---

# 🛠 Tech Stack

| Component | Technology |
| :--- | :--- |
| **Frontend/App** | Streamlit |
| **Language** | Python 3.10+ |
| **Database** | MongoDB Atlas (Pymongo) |
| **ML/NLP** | Hugging Face Transformers, PyTorch |
| **Authentication** | PyJWT, Bcrypt, Google Auth |
| **Visualization** | Plotly Express, Plotly Graph Objects |
| **Deployment** | Ngrok (Tunneling), Docker (Optional) |
| **Email Services** | Simple Mail Transfer Protocol(SMTP Gmail) |

---

# 🤖 Models Used

| Model | Use Case | Notes |
| :--- | :--- | :--- |
| **DeepSeek-Coder-1.3B** | Code Generation | High performance on logic generation. |
| **Microsoft Phi-2** | General Chat & Logic | Lightweight, efficient reasoning model. |
| **CodeBART-Base** | Code Summarization | Used for non-Python explanations. |
| **Python AST** | Structural Analysis | Native Python library for Abstract Syntax Trees. |

---

# 📂 Project Structure

```text
CodeGenie/
├── app.py                 # Main application entry point (Streamlit)
├── utils/
│   ├── db.py              # MongoDB connection logic
│   └── __init__.py
├── chat_history/          # JSON storage for chat sessions
├── .env                   # Environment variables (Secrets)
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```
---

## ❄️ Installation & Setup

### **Prerequisites**
-  Python 3.10 or higher
- MongoDB Atlas Account (Connection String)
- Google Cloud Console Project (For OAuth - Optional)
- Git
- (Optional) Docker

---

### **Clone & Install**
```bash
1)clone & Install:

git clone <repo-link>
cd Infosys_Springboard_CodeGenie
pip install -r requirements.txt
# Core libs: streamlit, pymongo, transformers, torch, bcrypt, pyjwt, google-auth
JWT_SECRET_KEY=your_key_here
SMTP_EMAIL=your_mail_here
SMTP_PASSWORD=your_app_pass_here

2)Configure Environment Variables:

Create a file named .env in the root directory:
MONGO_URI="mongodb+srv://<user>:<pass>@cluster.mongodb.net/..."
JWT_SECRET="YourSuperSecretKey"
HUGGINGFACE_TOKEN="hf_..."

# Google OAuth (Optional)
GOOGLE_CLIENT_ID="your_google_client_id"
GOOGLE_CLIENT_SECRET="your_google_client_secret"
APP_BASE_URL="http://localhost:8501"

# Email SMTP (For OTP)
SMTP_HOST="smtp.gmail.com"
SMTP_PORT="587"
SMTP_USER="your_email@gmail.com"
SMTP_PASS="your_app_password"
EMAIL_FROM="CodeGenie <no-reply@codegenie.ai>"

# Admin Setup
ADMIN_INITIAL_USER="admin@codegenie.com"
ADMIN_INITIAL_PASS="admin123"

3)Run Project
streamlit run app.py

```

# 📝 Usage Guide

1. **Sign Up / Login:** Create an account via Email/OTP or sign in with Google.

2. **Select Module:**
   -Go to 💻 Workspace to Generate or Explain code.
   -Go to 🧠 General Chat to talk to the AI assistant.

3. **Generate:** Select "Generate Code", choose a model (e.g., DeepSeek), pick a language, and type your prompt.

4. **Explain:** Select "Explain Code", paste your snippet, and get an AST breakdown or AI summary.

5. **Review:** Rate the output (1-5 stars) to help improve the system.

6. **History:** Check the ⟲ History tab to revisit past code snippets.
---

# 🛡 Admin Controls
**1. User Management**
Admins have full control over the user base to ensure security and manage access levels.
- **Role Management:** Admins can promote standard users to "Admin" status or revoke admin privileges from existing admins
- **Account Suspension:** Admins can suspend or unsuspend user accounts, effectively blocking or restoring their access to the platform
- **User Deletion:** There is functionality to permanently delete user accounts from the database
- **Search & Filter:** Admins can search for specific users by username and filter the user list by role (Admin vs. User)

**2. Request Handling**
This module manages requests from users who want elevated privileges (e.g., requesting Admin access).
- **Review Requests:** View a list of pending requests, including the user's reason for the request and the timestamp
- **Approve/Reject:** Admins can explicitly approve or reject these requests. The system updates the request status and logs the action
- **Reset Status:** Ability to mark a request back to "Pending" if it needs re-evaluation

**3. Analytics Dashboard**
The admin panel includes a visualization suite to monitor system health and usage trends.
- **User Growth:** A line chart displaying user signups over time
- **Login Activity:** A bar chart showing daily login counts
- **Model Popularity:** A pie chart illustrating which AI models (e.g., DeepSeek, Phi-2) are most frequently used
- **Activity Heatmap:** A heatmap showing user activity intensity by day of the week and hour of the day
- **Generations vs. Explanations:** A comparative chart showing the volume of code generation requests versus explanation requests

**4. System Logs & Security**
For auditing and security purposes, the admin panel provides deep visibility into system operations.
- **Action Logging:** A searchable log viewer that tracks critical actions such as logins, failed authentication attempts, file uploads, password changes, and admin actions
- **Filter Logs:** Logs can be filtered by username and date range to investigate specific incidents
- **Export Logs:** Capability to download system logs as a CSV file for external analysis

**5. Content Moderation (Reviews)**
Admins can oversee user feedback to maintain quality and address issues.
- **View Reviews:** Access a list of all user-submitted reviews, including ratings (1-5 stars) and written feedback
- **Delete Reviews:** The ability to remove specific reviews from the system

**6. Data Export**
To support reporting and external data analysis, the admin panel offers export functionality.
- **CSV Exports:** One-click download of entire collections, including Users, History, Reviews, Requests, and Files
- **PDF Reports:** If the `reportlab` library is installed, admins can generate formatted PDF reports of the user base

---

# 📊 History & Analytics

**User History:** Every generation or explanation is stored with:
- Timestamp
- Model Used
- Response Time (ms)
- Result & Prompt
  
**Admin Dashboard:** Admins can visualize:
- 📈 User Growth: Line charts of signups.
- 🥧 Model Usage: Pie charts showing which AI models are most popular.
- 🔥 Activity Heatmap: When users are most active during the week.
- 📝 Logs: System-wide audit logs for security.
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

