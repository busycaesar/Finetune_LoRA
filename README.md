# Finetune LoRA

## Description

Fine-tuning Google's Gemma 3 1B Instruct model using LoRA (Low-Rank Adaptation) on the [Databricks Dolly 15K](https://huggingface.co/datasets/databricks/databricks-dolly-15k) dataset. The notebook runs on Google Colab using a JAX backend.

## Tech Stack

![Image Alt](https://skillicons.dev/icons?i=py)

## Features

- Loads `gemma3_instruct_1b` from Keras Hub
- Enables LoRA with rank 4 to reduce trainable parameters
- Trains on 1,000 examples from Databricks Dolly 15K (no-context entries only)
- Sequence length capped at 256 tokens
- AdamW optimizer (lr=5e-5, weight decay=0.01)
- TopK sampling (k=5) for text generation

## How to run the project?

1. Open the notebook in Google Colab using the badge at the top of `gemma.ipynb`
2. Add your Kaggle credentials (`KAGGLE_USERNAME` and `KAGGLE_KEY`) to Colab Secrets
3. Run all cells in order — the notebook will install dependencies, download the dataset, fine-tune the model, and generate a sample response

## Author

[Dev J. Shah](https://github.com/busycaesar)
