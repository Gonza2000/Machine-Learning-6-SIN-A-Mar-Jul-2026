FROM python:3.13-slim

# Instalación de dependencias del sistema
RUN apt-get update && apt-get install -y \
    curl \
    git \
    git-lfs \
    && rm -rf /var/lib/apt/lists/*

RUN git lfs install --system

# Instalación de UV
RUN curl -LsSf https://astral.sh/uv/install.sh | sh
ENV PATH="/root/.local/bin:$PATH"

# Directorio de trabajo estándar para Codespaces/DevContainers
WORKDIR /workspaces/Machine-Learning-6-SIN-A-Mar-Jul-2026

# Copiar archivos de dependencias PRIMERO (para aprovechar el cache de Docker)
COPY pyproject.toml uv.lock ./

# Crear el venv con el nombre estándar que pide el profe
RUN uv venv .venv

# Instalar dependencias usando el flag obligatorio --python
# IMPORTANTE: Usamos -r pyproject.toml para instalar las dependencias listadas
RUN uv pip install --python .venv/bin/python -r pyproject.toml

# Variables de entorno para que el sistema reconozca el venv
ENV VIRTUAL_ENV=/workspaces/Machine-Learning-6-SIN-A-Mar-Jul-2026/.venv
ENV PATH="/workspaces/Machine-Learning-6-SIN-A-Mar-Jul-2026/.venv/bin:$PATH"
