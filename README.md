# Infosys_Springboard
Developing 'CodeGenie,' an AI assistant for code explanation and generation, leveraging advanced NLP techniques. An Infosys Springboard project.



# Infosys CodeGenie Project
### An AI-Powered Code Explainer and Generator

![Status](https://img.shields.io/badge/status-in_progress-yellow)
![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)



## 1. Project Overview

Welcome to the repository for the **CodeGenie** project, developed as part of the Infosys Springboard program. This project is an exploration into building an intelligent AI assistant designed to provide nuanced, context-aware analysis and generation of software code.

#### The Problem
Modern development relies heavily on understanding large, complex codebases. While general-purpose AI assistants are powerful, they often lack the specific context of a given project, leading to generic suggestions. Furthermore, different AI models can provide varied explanations for the same code, and understanding these differences is key to leveraging them effectively.

#### The Solution
CodeGenie is designed to address these challenges. It's a Python-based tool that will ultimately be able to:
* **Explain code** with a deep understanding of its structure and purpose.
* **Compare** the analytical "personas" of different NLP models.
* **(Future Goal)** **Generate** new, contextually relevant code snippets.



## 2. Key Features (Current)

As of Milestone 1, the project has the following capabilities:

* **Object-Oriented Design**: A modular and scalable `CodeExplainer` class encapsulates all core logic.
* **Line-by-Line Code Analysis**: Processes Python scripts line by line to generate targeted explanations.
* **Comparative Model Simulation**: Utilizes a template-based system to simulate and compare the distinct explanatory styles of three different NLP models (MiniLM, DistilRoBERTa, MPNet).
* **Structured Reporting**: Leverages the `pandas` library to generate clean, readable, side-by-side comparison tables of the model outputs.



## 3. Repository Structure & Milestones

This project is developed through a series of milestones. Each has a dedicated folder containing its specific code, documentation, and findings.

* ### [Milestone 1: Code Explainer](./Milestone1/)
    * **Objective:** Build a pipeline to generate and compare line-by-line explanations for Python code snippets using a template-driven approach.
    * **Status:** ✅ **Complete**

* ### `Milestone 2: Code Generation Engine`
    * **Objective:** *(To be defined)*
    * **Status:** ⚪ **Planned**



## 4. Technology Stack

This project utilizes a modern stack of data science and Python libraries:

* **Primary Language:** **Python**
* **Core Libraries:**
    * **Pandas:** For data manipulation and creating structured comparison tables.
    * **Sentence-Transformers:** For loading and interfacing with pretrained NLP models.
* **Code Analysis Tools:**
    * **AST (Abstract Syntax Tree):** For programmatic analysis of Python code structure.
    * **Tokenize:** For breaking code down into its fundamental lexical units.
* **Development Environment:** **Google Colaboratory**


