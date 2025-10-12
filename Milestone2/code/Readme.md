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


