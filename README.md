# LLM-Log-Analysis-Evaluation
An evaluation of the Mistral-7B Large Language Model on various log analysis tasks including parsing, summarization, and anomaly detection.
This project presents a comprehensive evaluation of the Mistral-7B-Instruct-v0.2 Large Language Model (LLM) on various log analysis tasks. The goal was to assess the LLM's performance against traditional methods in key areas like log summarization, parsing, anomaly detection, and fault diagnosis.
Key Features:

Multi-task Evaluation: The Mistral model's performance was evaluated on four critical log analysis tasks: log parsing, log summarization, log fault diagnosis, and anomaly detection.


Traditional Method Comparison: The project compares the summarization capabilities of the LLM against older, traditional methods like LSA and TextRank, demonstrating a clear performance advantage for the LLM.
Prompt Engineering: The study explores the impact of different prompting techniques. It compares custom-developed prompts with the original prompts from the research paper to find the most effective approach for each task. 

Resource Optimization: To enable the execution of a large model like Mistral-7B in a resource-constrained environment (such as Google Colab), the project utilizes 4-bit quantization. This method significantly reduces memory usage with minimal performance trade-offs. 

Project Structure
notebooks/: Contains the Jupyter Notebook files for the evaluations.


mainlogeval_(1).ipynb: The primary code for evaluating the Mistral-7B model on all four log analysis tasks using the original prompts. 


promptslogeval_(1).ipynb: This notebook evaluates the model using custom-designed prompts to test their effectiveness. 
traditionallogeval_(1).ipynb: A notebook dedicated to evaluating traditional summarization methods (LSA and TextRank) on the log summarization dataset. 


comparinglogeval_(1).ipynb: This file provides a visual comparison and analysis of the results between the LLM and the traditional summarization methods. 

dataset/: This directory contains the datasets used for the evaluation, cloned from the original paper's repository.

requirements.txt: Lists all necessary Python libraries for replicating the project environment.

Key Findings
The results largely align with the original paper's findings, while also providing new insights:


LLM vs. Traditional Methods: The Mistral model consistently outperformed traditional methods like LSA and TextRank in log summarization, as demonstrated by superior F1-scores and Cosine Similarity metrics. 
Prompting Impact: Simple and direct prompts from the original paper were generally more effective than the more complex or role-playing custom prompts. However, one of the custom prompts designed for pattern detection achieved a similar Cosine Similarity score, indicating the potential for tailored prompts in specific scenarios. 

Zero-shot vs. Few-shot: Few-shot learning generally improved the model's performance across most tasks. A notable exception was anomaly detection, where the few-shot approach yielded worse results, possibly because the model overfitted or memorized the examples.
Language Performance: The model's performance varied by language. It showed better results in some tasks in English and in others in Chinese. 

How to Run
To replicate this project, follow these steps:

Clone the repository.

Install the dependencies listed in requirements.txt.
pip install -r requirements.txt
Execute the Jupyter Notebooks in the notebooks/ folder. It's recommended to run mainlogeval_(1).ipynb first to establish a baseline, then the other notebooks for further comparisons. The comparinglogeval_(1).ipynb notebook can be run last to visualize and analyze all results.
