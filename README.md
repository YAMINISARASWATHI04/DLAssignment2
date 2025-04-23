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

## Run the model training and evaluation:
```
python marathi_transliteration_seq2seq.py
```
## Code Structure
-load_data(path): Loads and cleans TSV files

-encode_sequences(): Tokenizes, encodes, and pads sequences

-build_seq2seq_model(): Constructs the encoder-decoder architecture

-decode_sequence(input_seq): Transliterates test samples


# 🎤 GPT-2 English Lyrics Generator

This repository contains an implementation to **fine-tune GPT-2** using Hugging Face Transformers to generate English song lyrics. It leverages datasets of English poetry and lyrics and trains a language model that generates creative, rhyming, and song-like text.

---

## 📁 Dataset

We use English poetry/lyrics datasets to train the model. Recommended datasets include:

- 🔗 [Kaggle - Poetry by Paul Mooney](https://www.kaggle.com/paultimothymooney/poetry)
- 🔗 [Lyrics on Data.World](https://data.world/datasets/lyrics)

Once downloaded, extract and organize the data into a folder like `./dataset/`, ensuring the file contains lines or entries of lyrics (preferably a `.txt` or `.csv` file with a `text` column).

Example:
```text
I saw the stars align above the sea  
Dancing lights and your eyes on me
```
# 🛠️ Setup Instructions
## 1. Clone the repository
bash
Copy
Edit
```
git clone https://github.com/yourusername/gpt2-lyrics-generator.git
cd gpt2-lyrics-generator

```

## 2. Install dependencies
-bash
-Copy
-Edit
```
pip install -r requirements.txt
```
requirements.txt should contain:

-nginx
-Copy
-Edit
-transformers
-datasets
-torch
-huggingface_hub
## 3. Hugging Face Authentication
Generate a token from https://huggingface.co/settings/tokens and choose Models access.

Then run:
```
bash
Copy
Edit
huggingface-cli login
Paste your token when prompted.
```

🧠 Model Training
To fine-tune GPT-2 on the lyrics dataset:
```
bash
Copy
Edit
python train.py
```
# This script will:

-Load the gpt2 model and tokenizer

-Tokenize your lyrics dataset

-Fine-tune the model

-Save the model to ./gpt2-lyrics/





