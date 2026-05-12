FROM python:3.12-slim

RUN apt-get update && apt-get install -y \
    curl \
    git \
    git-lfs \
    && rm -rf /var/lib/apt/lists/*

RUN git lfs install --system
RUN curl -LsSf https://astral.sh/uv/install.sh | sh
ENV PATH="/root/.local/bin:$PATH"

WORKDIR /app

RUN uv venv .gabriel

COPY pyproject.toml uv.lock ./

RUN  uv pip install --python .gabriel/bin/python .

ENV VIRTUAL_VENV=/app/.gabriel
ENV PATH="/app/.gabriel/bin:$PATH"
