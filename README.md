# Human Value Integrated Agent using the Schwartz Value Framework

A value-aware AI system that predicts human values from text, selects policy decisions based on configurable agent profiles, and generates natural-language justifications.

## Team
- Anya Arun Gupta — CS24MTECH11020
- Khushbu Chaudhary — CS24MTECH14012

---

# Project Overview

Most AI systems optimize only for accuracy or efficiency.  
This project introduces a **Human Value Integrated Agent** that makes decisions using human values such as:

- Benevolence
- Power
- Security
- Openness
- Universalism
- Tradition
- Achievement
- and others

We use the **Schwartz Value Theory** and the **Touché ValueEval Human Values Dataset**.

The system pipeline:

1. Predict values from text arguments
2. Aggregate fine-grained values into broader categories
3. Compare candidate options with agent preferences
4. Select the best option
5. Generate a persuasive explanation using an LLM

---

# Models Used

## 1. Baseline Model
- all-MiniLM-L6-v2
- Logistic Regression

## 2. Improved Models
- DeBERTa-v3-small
- RoBERTa-base

## 3. Justification Generator
- Mistral 7B Instruct (4-bit)

---

# Dataset

Touché ValueEval Human Values Dataset

Used files:
- arguments-training.tsv
- arguments-validation.tsv
- level1-labels-training.tsv
- level1-labels-validation.tsv
- value-categories.json

---

# Results

| Model | Micro F1 | Macro F1 |
|------|----------|----------|
| MiniLM + LR | 0.4526 | 0.4073 |
| DeBERTa | 0.5380 | 0.3790 |
| RoBERTa | 0.5698 | 0.4494 |

---

# Repository Structure

```text
project/
│── TDL_cs24mtech11020_cs24mtech14012.ipynb
│── report.pdf
│── flowchart.png
│── README.md
