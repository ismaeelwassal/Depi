# Depi – Clinical Note Intelligence Pipeline 📋
## Overview
Depi is a compact, end‑to‑end demo that shows how to build an **LLM‑powered clinical note classification and extraction** workflow. It uses a public Kaggle transcription dataset, cleans the text, engineers specialty labels, draws a stratified sample, runs a Groq‑hosted LLM for classification, falls back to a simple baseline when needed, extracts structured fields, and finally evaluates the results in an interactive dashboard.

## Key Features
- **Data preparation** – automatic cleaning of raw transcriptions.
- **Label engineering** – maps raw specialties to a curated set of 29 categories.
- **Stratified sampling** – guarantees every specialty appears in the sample.
- **LLM classification** – Groq API call with retry logic.
- **Fallback baseline** – deterministic rule‑based classifier.
- **Extraction** – Pydantic‑validated note parsing.
- **Evaluation & dashboard** – precision/recall metrics visualised with seaborn/matplotlib.

## Quick Start
```bash
# Clone & enter the repo
git clone https://github.com/gadjicte/Depi.git && cd Depi

# Create a virtual environment (Python 3.13)
python -m venv .venv && source .venv/bin/activate

# Install dependencies
pip install -r requirments.txt

# Set your Groq API key (create .env if missing)
export GROQ_API_KEY=YOUR_KEY

# Run the notebook (or JupyterLab)
jupyter notebook clinical.ipynb
