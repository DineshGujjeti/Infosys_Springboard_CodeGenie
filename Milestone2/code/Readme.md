# Code Generation Benchmark with Pretrained AI Models

This project implements a benchmarking system for code generation AI models using pretrained models from Hugging Face. It evaluates generated code based on complexity, maintainability, and lines of code (LOC), providing interactive user interfaces and visualizations of model performance.

## Features

- **Pretrained Models Benchmarked:**
  - DeepSeek-Coder-1.3B (`deepseek-ai/deepseek-coder-1.3b-instruct`)
  - Phi-2-2.7B (`microsoft/phi-2`)
  - Gemma-2B-IT (`google/gemma-2b-it`)

- **Evaluation Metrics:**
  - **Code Complexity:** Assessed via cyclomatic complexity using the Radon library.
  - **Maintainability:** Calculated using the maintainability index from Radon.
  - **Lines of Code (LOC):** Basic count of code lines.

- **Sample Prompts:**
  - 10 diverse code generation prompts from various programming domains, including recursive functions, data processing, algorithms, web apps, and scripting.

- **Interactive Google Colab UIs:**
  - **UI #1:** Benchmark all models with prompts and visualize aggregated metric results.
  - **UI #2:** Inspect generated code from selected models for any prompt using checkboxes.

- **Visualizations:**
  - Bar plots comparing models based on average LOC, complexity, and maintainability.
 
- ## Summary

This project provides a framework to systematically compare state-of-the-art code generation models on standardized prompts and metrics. The interactive UIs aid in detailed inspection, while visualizations facilitate quick performance comparisons. It serves as a baseline for further research and improvements in AI-assisted coding.


## Usage Instructions

### 1. Open in Colab
- Open the notebook `Milestone2.ipynb` in [Google Colab]([https://colab.research.google.com/](https://colab.research.google.com/drive/1_7hT3piuAiKIs6GUvGox0FmOIB1NWSlg?usp=sharing).
- Run all cells to generate outputs.

- ## **Outputs**
- **Setup and Installations:**
- <img width="789" height="89" alt="image" src="https://github.com/user-attachments/assets/85adb540-0161-46e1-b165-0552b9d1c368" />

- **Secure Hugging Face Login:**
<img width="337" height="32" alt="image" src="https://github.com/user-attachments/assets/de6537bc-55db-46c8-9214-4be3ee77be74" />

- **Configuration & Backend Engine:**
<img width="457" height="35" alt="image" src="https://github.com/user-attachments/assets/19b515c4-42e6-4f24-8ccd-b4e66ef0411e" />

- **Pre-Loading All AI Models:**
<img width="959" height="837" alt="image" src="https://github.com/user-attachments/assets/3d7d0656-94a1-4780-927a-6d21115e7d54" />
<img width="1135" height="400" alt="image" src="https://github.com/user-attachments/assets/5adae6e2-327f-437f-89f4-ee90a6a0da5b" />


- **UI #1:**
- <img width="1722" height="621" alt="image" src="https://github.com/user-attachments/assets/d719ed27-11b2-4ae4-8b9c-0a0cc8a986aa" />

- **UI #2:**
- <img width="1849" height="620" alt="image" src="https://github.com/user-attachments/assets/5ad28d66-a960-4a41-8c19-53d95f5009a5" />

- **Final Analysis and Visualization Report:**
<img width="1285" height="616" alt="image" src="https://github.com/user-attachments/assets/5f7b0960-27ac-481d-bacc-87a62686e181" />










