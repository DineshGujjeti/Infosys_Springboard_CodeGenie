# Milestone 1: Code Explainer 

This document provides a detailed overview of the first milestone for the **Infosys CodeGenie Project**. This milestone focuses on the design and implementation of a proof-of-concept pipeline that can automatically generate and compare line-by-line explanations for Python code snippets.

## 1. Problem Statement

Developers and programmers often spend a significant amount of time trying to understand unfamiliar codebases. While AI assistants can help, their explanations can be generic. Furthermore, different AI models may interpret and explain the same line of code in subtly different ways. This project aims to build a tool that not only explains code but also highlights these nuanced differences between AI model "personas."

## 2. Approach and Methodology

To achieve the project's objective, a template-driven, object-oriented approach was implemented in a Python notebook. This methodology is broken down into the following key components:

#### 2.1. Object-Oriented Design
The core logic is encapsulated within a `CodeExplainer` class. This design choice makes the code modular, easy to maintain, and scalable for future milestones. It cleanly separates concerns such as model loading, explanation generation, and report formatting.

#### 2.2. Template-Based Explanation Generation
A key feature of this pipeline is the `explanation_templates` dictionary. This structure holds predefined explanation patterns with unique phrasing for each of the three simulated models (`MiniLM`, `DistilRoBERTa`, `MPNet`). This simulates how different AI models might have distinct linguistic styles, creating unique analytical "personas." For example, a variable assignment is explained differently by each model:
* **MiniLM**: `Assigns value to 'variable_name'`
* **DistilRoBERTa**: `Sets variable 'variable_name' to a value`
* **MPNet**: `Stores result in 'variable_name'`

#### 2.3. Rule-Based Line Analysis
The `explain_line` method processes each line of a code snippet using a rule-based system. It checks for specific keywords and symbols (e.g., `def`, `class`, `=`, `if`) to determine the line's purpose. Once identified, it matches the line to the appropriate template from the `explanation_templates` dictionary to generate the corresponding explanation for each model.

#### 2.4. Structured Comparative Reporting
The powerful `pandas` library is leveraged to structure the final output. For each code snippet, a DataFrame is constructed. This table presents the line number, the original code, and the generated explanations from all three models in a clean, side-by-side format, allowing for easy and direct comparison.

## 3. Technical Details

* **Key Modules Used:**
    * `pandas`: For creating, manipulating, and displaying the final comparison tables (DataFrames).
    * `sentence-transformers`: For loading the pretrained NLP models which serve as the basis for the AI personas.
    * `io` / `tokenize`: (Used in earlier analysis stages) For breaking down code into its fundamental tokens.
    * `ast`: (Used in earlier analysis stages) For parsing code into an Abstract Syntax Tree to analyze its structure.

## 4. Observations and Results

The implemented pipeline successfully generated distinct, line-by-line explanations for all test snippets. The results highlight several key points:

* **Effective Persona Simulation**: The template system is highly effective at creating distinguishable "personas" for each model. The consistent use of different verbs and sentence structures for the same type of code line makes the comparison clear and meaningful.

* **Clarity of Output**: The use of pandas DataFrames is a major strength, presenting the complex, multi-model comparison in a format that is both human-readable and easy to analyze.

* **Limitations**: As a proof-of-concept, the current system is rule-based and does not possess true semantic understanding. Its explanations are derived from templates, not from a deep comprehension of the code's logic. Therefore, it cannot explain the *purpose* or *outcome* of the code, only its syntactic structure.

## 5. Future Work

This milestone serves as a strong foundation for future development. Potential next steps include:
* **Integration of a Generative LLM**: Replace the template-based system with a true Large Language Model (e.g., from the GPT or T5 family) to generate dynamic, context-aware explanations.
* **Expanding Pattern Recognition**: Enhance the rule-based system to recognize a wider variety of complex Python syntax, such as decorators, context managers, and advanced exception handling.
* **Semantic Similarity Analysis**: Use the loaded embedding models to find semantically similar code snippets across a larger codebase and compare their explanations.
