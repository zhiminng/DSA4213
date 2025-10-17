# DSA4213

# Financial Sentiment Analysis: Full Fine-tuning vs LoRA

This project compares **Full Fine-tuning** and **LoRA (Low-Rank Adaptation)** for financial sentiment classification using the **FinancialPhraseBank** dataset and FinBERT.

---

## Dataset

The dataset used is the **Financial PhraseBank** (`Sentences_66Agree.txt`), which contains financial news sentences labeled with positive, neutral, or negative sentiment.  

**Download path**:  
FinancialPhraseBank-dataset/
└── FinancialPhraseBank-v1.0/
└── Sentences_66Agree.txt


---

## How to Run

### 1️.Download the Notebooks
- `Full_Finetuning.ipynb`  
- `LoRA.ipynb`  

### 2️.Open in Google Colab
Upload the notebooks to **Google Colab**.

### 3️.Upload the Dataset
Manually upload `Sentences_66Agree.txt` in Colab before running the notebooks.

### 4️.Run All Cells
Each notebook will:
- Load and preprocess the dataset
- Fine-tune FinBERT (full or LoRA)
- Evaluate accuracy, F1-scores, and per-class metrics
- Plot training vs. validation loss

---

## Results Summary

| Method            | Accuracy | Notes |
|------------------|---------|--------------------------------|
| Full Fine-tuning  | ~86%    | All 110M parameters trained, strong performance |
| LoRA              | ~51%    | Only 0.27% of parameters trained, requires careful tuning |

---

## Key Takeaways

- **Full fine-tuning** achieves higher performance on small-to-medium datasets.  
- **LoRA** offers huge parameter efficiency but is sensitive to rank, learning rate, training duration, and target modules.  
- Using **FinBERT** as the base model provides strong domain-specific initialization.  
- Parameter-efficient methods like LoRA are promising for resource-constrained environments but need careful engineering.

---

