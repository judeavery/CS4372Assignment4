CS4372 Assignment 4 – Transformers

Student: Jude Avery
Course: CS 4372 – Computational Methods for Data Scientists
Instructor: Anurag Nagar

Project Overview

This project uses a pretrained Transformer model from the Hugging Face transformers library to perform machine translation (English → Spanish) on text from a public domain book hosted on Project Gutenberg. The goal is to apply a modern encoder–decoder Transformer to real-world text, explore how different hyperparameters affect the output, and evaluate translation quality using BLEU.

Task: Machine Translation (EN → ES)

Book: Romeo and Juliet by William Shakespeare

Data Source: Project Gutenberg (direct text URL)

The entire workflow—including dataset loading, preprocessing, translation, and evaluation—was implemented in a single Google Colab notebook.

Dataset

The dataset is the public-domain book Romeo and Juliet accessed directly from this URL:

https://www.gutenberg.org/files/349/349-0.txt


The file is downloaded programmatically inside the notebook using requests.get().
This follows the assignment requirement to avoid local file paths and rely only on global URLs.

Model

This project uses the following pretrained translation model:

Helsinki-NLP/opus-mt-en-es

This is an encoder–decoder Transformer trained specifically for English→Spanish translation and is fully compatible with the Hugging Face pipeline API.

Repository Structure
CS4372Assignment4/
│
├── CS4372Assignment4.ipynb      # Main Colab notebook with all code and experiments
├── README.md                    # Project documentation (this file)
├── requirements.txt             # Python dependencies
│
├── report/
   └── CS4372_Assignment4_Report.pdf   # Final project report (PDF)


How to Run
1. Open the Notebook

Open CS4372Assignment4.ipynb in Google Colab.

2. Install Dependencies

Run the installation cell or manually install requirements:

pip install -r requirements.txt

3. Run the Notebook Cells in Order

The notebook will:

Download the Romeo and Juliet text from Project Gutenberg

Clean and preprocess the text

Set up the Transformer translation pipeline

Translate sample passages

Test multiple hyperparameter configurations

Evaluate translations using BLEU (via sacrebleu)

Print quantitative and qualitative results

All results shown in the final report can be reproduced by running the notebook top-to-bottom.

Dependencies

The required packages are listed in requirements.txt:

transformers
torch
datasets
evaluate
rouge-score
sacrebleu


All packages are available via pip and run smoothly in Google Colab.

Report

The full written report summarizing:

Data sourcing

Transformer architecture

Model selection

Experiment setup

BLEU evaluation

Hyperparameter impact

Translation examples

Discussion & Conclusion
