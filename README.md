# Infosys_Springboard
Developing 'CodeGenie,' an AI assistant for code explanation and generation, leveraging advanced NLP techniques. An Infosys Springboard project.
# Infosys Springboard - Milestone 1: Code Explainer

This repository contains the implementation for the milestone of the CodeGenie project. The objective is to build a pipeline that analyzes Python code snippets, generates semantic embeddings using various transformer models, and visually compares their understanding of the code.

---

## Approach and Methodology

The project was executed following a structured pipeline:

1.  **Data Preparation**: A diverse set of 10+ Python code snippets was curated. This collection includes simple functions, class definitions, file I/O operations, and examples using libraries like Pandas and NumPy to ensure a comprehensive evaluation of the models.

2.  **AST Parsing**: Python's built-in `ast` (Abstract Syntax Tree) module was used to parse each snippet. This allowed for the programmatic extraction of key structural elements like function names, class names, and imported libraries, providing a structured summary of the code's components.

3.  **Embedding Generation**: The `sentence-transformers` library was utilized to load three distinct pretrained models: `all-MiniLM-L6-v2`, `all-distilroberta-v1`, and `all-mpnet-base-v2`. Each model processed the raw code snippets to generate high-dimensional vector embeddings that capture their semantic meaning.

4.  **Visualization and Comparison**: To visually compare the models' understanding of the code, the dimensionality of the embeddings was reduced to 2D using **PCA** (Principal Component Analysis). Scatter plots were then generated for each model, illustrating how they clustered the different code snippets in a 2D space.

---

