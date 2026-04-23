# AI/ML Project Scaffold

## About
This project serves as a simple scaffold for small/medium-sized AI/ML projects. It uses **uv** as the main package manager for fast, reproducible environment management.

---

## Project Structure

The project follows a modular structure to separate data, experimentation, and production-ready source code:

```text
aiml-project-scaffold/
├── data/               # Local datasets (raw, processed, or interim)
├── models/             # Model checkpoints, weights, and serialized artifacts
├── notebooks/          # Jupyter notebooks for EDA and prototyping
├── src/                # Core logic, data loaders, and model architectures
├── .env                # Environment variables (API keys, secrets)
├── .gitignore          # Git exclusion rules
├── .python-version     # Target Python version (managed by uv)
├── main.py             # Main entry point for training or inference
├── pyproject.toml      # Dependency definitions and project metadata
├── README.md           # Project documentation
└── uv.lock             # Deterministic lockfile for dependencies
```

## Getting Started

### 1. Prerequisites
Ensure you have [uv](https://github.com/astral-sh/uv) installed:
```bash
curl -LsSf [https://astral-sh.com/uv/install.sh](https://astral-sh.com/uv/install.sh) | sh
```

### 2. Installation
Install the project dependencies and create a virtual environment automatically:
```bash
uv sync
```

### 3. Usage
- **Run the main script:**
  ```bash
  uv run main.py
  ```
- **Development:**
  The `.venv` directory is created locally, making it easy to point VS Code or PyCharm to the correct interpreter.

## Configuration
- Store sensitive credentials (like API keys) in the `.env` file.
- Manage dependencies by adding them via `uv add <package_name>`.