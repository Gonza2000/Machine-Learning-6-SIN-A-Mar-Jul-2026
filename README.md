# Proyecto Final de Parcial 2

## Integrantes
Gonzalo Cárdenas & Gabriel Vásquez

## Dataset Choice
We selected the **Titanic Survivor Dataset** as it provides an excellent mix of categorical and numerical features for a fundamental classification problem. The data is clean enough for quick prototyping but still requires careful preprocessing and feature engineering. It allows us to experiment with various models and easily interpret the survival rate predictions. The manageable dataset size makes it ideal for a reproducible, containerized environment workflow.

## Tool Justification
We chose **VS Code Devcontainers** to guarantee absolute environment reproducibility across any machine that runs Docker, eliminating the "it works on my machine" problem. **uv** was selected as our package manager and resolver due to its blazing-fast performance compared to standard pip and its excellent dependency locking capabilities (`uv.lock`). We explicitly build our environments utilizing standard Python slim images because they are lightweight and have low attack surfaces. This tooling stack ultimately ensures that running our analytical notebooks requires zero manual configuration from the reviewer.

## How to Clone and Run
To replicate our results, run the following three commands (make sure Docker and VS Code are installed):

```bash
git clone https://github.com/jonathanetitoo/Machine-Learning-6-SIN-A-Mar-Jul-2026.git
cd Machine-Learning-6-SIN-A-Mar-Jul-2026
code .
```
*Once VS Code opens, click **"Reopen in Container"** when prompted, and run the `notebooks/main.ipynb` notebook top-to-bottom.*

## Results Summary

| Model / Analysis        | Metric                 | Result |
|-------------------------|------------------------|--------|
| Baseline Survival Rate  | Mean Survival Accuracy | 60.00% |
| Dataset Size            | Rows                   | 5      |
| Sample Features Used    | Age, Pclass, Sex       | N/A    |

## AI Usage Disclosure
AI (Gemini / Code Agent) was used to structure this repository, help write the Dockerfile, generate the boilerplate devcontainer configurations, and formulate the base environment setup to meet the strict reproducibility requirements of this workshop.
