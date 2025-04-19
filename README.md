# DLAssignment2

# 📝 Marathi Seq2Seq Transliteration Model

This repository contains an implementation of a character-level Seq2Seq (Encoder-Decoder) model using LSTM for transliterating Marathi text written in Latin script into Devanagari script. The model is trained and evaluated using the [Dakshina dataset](https://github.com/google-research-datasets/dakshina) by Google Research.

---

## 📁 Dataset

We use the **Marathi (mr)** transliteration subset of the Dakshina dataset. You can download it from the following link:

🔗 [Dakshina Dataset - GitHub](https://github.com/google-research-datasets/dakshina)

Once downloaded, place the following files in a folder such as `./data/`:
- `mr.translit.sampled.train.tsv`
- `mr.translit.sampled.dev.tsv`
- `mr.translit.sampled.test.tsv`

Each `.tsv` file has the format:
- Column 1: Target (native script, e.g., देवनागरी)
- Column 2: Input (Latin script)
- Column 3: Frequency (can be ignored)

---

## 🛠️ Setup Instructions

### 1. Clone the repository (or use your script directly)
### 2. Install dependencies:
```bash
pip install numpy pandas tensorflow nltk
