# CS4372Assignment4

# CS4372 Assignment 4 – Transformers

**Student:** Jude Avery  
**Course:** CS 4372 – Introduction to Machine Learning  
**Instructor:** (fill in)

## Project Overview

This project uses a pretrained Transformer model from the Hugging Face `transformers` library
to perform an NLP task on a public domain book from Project Gutenberg.

- **Task:** (e.g., text summarization / machine translation / question answering / text generation)
- **Book:** (Title, Author)
- **Data Source:** Project Gutenberg – direct text URL

## Repository Structure

- `CS4372Assignment4.ipynb` – main Colab notebook with all code and experiments
- `requirements.txt` – Python dependencies
- `report/` – final written report (PDF or source)
- `data/` (optional, small helper files only; main book is loaded via URL)

## How to Run

1. Open `CS4372Assignment4.ipynb` in Google Colab.
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
Run the notebook cells in order. The notebook will:

Download the book from Project Gutenberg via URL

Preprocess the text

Run the Transformer model for the chosen task

Evaluate outputs with suitable metrics

yaml
Copy code

You can tweak later when we know the exact task & model.

---

### 0.2 Add `requirements.txt`

Create a file in the repo called `requirements.txt` with:

```txt
transformers
torch
datasets
evaluate
rouge-score
sacrebleu
