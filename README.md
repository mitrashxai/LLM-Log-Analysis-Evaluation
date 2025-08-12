
# Evaluation of the Mistral-7B Large Language Model on Log Analysis Tasks

This project presents a comprehensive evaluation of the **Mistral-7B-Instruct-v0.2 Large Language Model (LLM)** on various log analysis tasks. The primary goal was to benchmark the LLM's performance against traditional methods and explore how different prompting techniques affect its output.

### **Project Highlights**

  * **Multi-task Evaluation:** We assessed the Mistral model's performance on four critical log analysis tasks: **Log Summarization**, **Log Parsing**, **Log Fault Diagnosis**, and **Anomaly Detection**.
  * **Comparison with Traditional Methods:** The project directly compares the LLM's summarization capabilities against classic, extractive methods like **LSA** and **TextRank**, demonstrating a clear performance advantage for the LLM.
  * **Prompt Engineering:** We explored the impact of different prompting techniques by comparing custom-designed prompts with the original prompts from the research paper. This allowed us to identify the most effective approaches for each task.
  * **Resource Optimization:** To enable the execution of a large model like Mistral-7B in a resource-constrained environment (such as Google Colab), the project utilizes **4-bit quantization**. This method significantly reduces memory usage with minimal performance trade-offs.

-----

### **Project Structure**

  * `notebooks/`: Contains the Jupyter Notebook files for all evaluations.
      * `main_evaluation.ipynb`: The primary code for evaluating the Mistral-7B model on all four log analysis tasks using the original prompts.
      * `prompt_engineering_evaluation.ipynb`: This notebook evaluates the model using custom-designed prompts to test their effectiveness.
      * `traditional_comparison.ipynb`: A dedicated notebook for evaluating traditional summarization methods (LSA and TextRank) on the log summarization dataset.
      * `results_comparison.ipynb`: This file provides a visual comparison and analysis of all the results.
  * `dataset/`: This directory contains the datasets used for the evaluation, cloned from the original LogEval paper's repository.
  * `requirements.txt`: Lists all necessary Python libraries for replicating the project environment.

-----

### **Key Findings**

The results of this project largely align with the original LogEval paper's findings while also providing new insights:

  * **LLM vs. Traditional Methods:** The Mistral model consistently outperformed traditional methods like LSA and TextRank in log summarization, as demonstrated by superior **F1-scores** and **Cosine Similarity** metrics.
  * **Prompting Impact:** Simple and direct prompts from the original paper were generally more effective than the more complex or role-playing custom prompts. However, one of the custom prompts designed for pattern detection achieved a similar Cosine Similarity score, indicating the potential for tailored prompts in specific scenarios.
  * **Zero-shot vs. Few-shot:** Few-shot learning generally improved the model's performance across most tasks. A notable exception was anomaly detection, where the few-shot approach yielded worse results, possibly because the model overfitted or memorized the examples.
  * **Language Performance:** The model's performance varied by language. It showed better results in some tasks in English and in others in Chinese.

-----

### **How to Run**

To replicate this project, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [Your Repository Link Here]
    cd [Your-Project-Folder-Name]
    ```
2.  **Install the dependencies** listed in `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```
3.  **Execute the Jupyter Notebooks** in the `notebooks/` folder. We recommend running `main_evaluation.ipynb` first to establish a baseline, then the other notebooks for further comparisons. The `results_comparison.ipynb` notebook can be run last to visualize and analyze all results.
focus on key findings effectively highlight your technical skills and insights.
pip install -r requirements.txt
