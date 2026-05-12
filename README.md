# Proyecto Final de Parcial 2

## Integrantes
Gonzalo Cárdenas & Gabriel Vásquez

---

## Dataset Choice

For this project, we selected the **Wine Quality Dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality?utm_source=chatgpt.com).  
This dataset contains physicochemical measurements of Portuguese “Vinho Verde” wines and their associated quality scores assigned by wine experts.

The dataset is especially valuable because it supports two different machine learning approaches:

- **Regression Task:** Predicting the wine quality score.
- **Classification Task:** Classifying wines as:
  - **Good wine:** quality ≥ 7
  - **Bad wine:** quality < 7

We chose this dataset because it offers:
- A realistic supervised learning problem.
- Multiple continuous numerical features suitable for exploratory analysis and feature engineering.
- Opportunities to compare regression and classification models within the same dataset.
- A manageable size that enables reproducible experimentation inside a containerized environment.

Additionally, the dataset is widely recognized in the machine learning community, making it ideal for benchmarking and educational purposes.

---

## Tool Justification

We utilized Pandas for efficient data manipulation and Scikit-learn to implement robust Linear and Logistic Regression models tailored for our physicochemical analysis. Our workflow is powered by uv and Docker Devcontainers to ensure extremely fast dependency resolution and a reproducible, isolated environment across any machine. This stack was chosen specifically to handle the dataset's numerical complexity while eliminating "it works on my machine" conflicts during the training phase. By combining these modern package managers with industry-standard ML libraries, we guaranteed a lightweight yet professional pipeline for all experiments.

## Clone and Run Instructions

To reproduce the environment and run the project, execute the following commands:
git clone
cd
devcontainer up --workspace

Enter the brach and get the link for cloning, the create the needed codespace

## AI Usage Disclosure

For this project, we integrated Gemini as a core technical assistant to streamline the development of the machine learning pipeline. Its usage was necessary to optimize the Python code structure, debug complex data transformations in Pandas, and refine the training scripts for our regression models, gemini provided critical support in automating repetitive boilerplate code and suggesting best practices for model evaluation.



---
