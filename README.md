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

We chose **VS Code Devcontainers** to ensure complete environment reproducibility across any machine capable of running Docker, eliminating the classic *“it works on my machine”* problem.

We selected **uv** as the package manager because of its:
- Extremely fast dependency resolution.
- Reliable lockfile generation (`uv.lock`).
- Lightweight and modern Python workflow.

Our environment is built using slim Python Docker images to:
- Reduce image size.
- Improve portability.
- Minimize attack surface and unnecessary dependencies.

This tooling stack guarantees that reviewers can reproduce all experiments, notebooks, and results with virtually zero manual configuration.

---
