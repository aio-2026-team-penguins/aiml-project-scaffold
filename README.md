# AI/ML Project Scaffold

## About
This project serves as a simple scaffold for small/medium-sized AI/ML projects. It uses **uv** as the main package manager and **Ruff** for high-performance linting and formatting.

---

## Project Structure

```text
aiml-project-scaffold/
├── data/               # Local datasets
├── models/             # Model checkpoints and weights
├── notebooks/          # Jupyter notebooks for EDA
├── src/                # Core logic and source code
├── .env                # Environment variables
├── .gitignore          # Git exclusion rules
├── .python-version     # Target Python version
├── .ruff_cache/        # Ruff's analysis cache for faster linting
├── main.py             # Main entry point
├── pyproject.toml      # Dependencies and Ruff configuration
├── README.md           # Project documentation
└── uv.lock             # Deterministic lockfile
```

---

## Getting Started

### 1. Prerequisites
Ensure you have [uv](https://github.com/astral-sh/uv) installed.

### 2. Installation
```bash
uv sync
```

### 3. Linting & Formatting
This project uses **Ruff** to maintain code quality. Configuration is handled within `pyproject.toml`.

* **Check for errors (lint):**
    ```bash
    uv run ruff check .
    ```
* **Auto-fix linting issues:**
    ```bash
    uv run ruff check --fix .
    ```
* **Format code:**
    ```bash
    uv run ruff format .
    ```

---

## Usage
Run the main pipeline:
```bash
uv run main.py
```

## Configuration
* **Dependencies:** Add new packages using `uv add <package>`.
* **Environment:** Add your secrets to `.env` (this file is git-ignored).