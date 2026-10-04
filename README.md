# 🧠 N-Gram Model & POS Tagging

## 📌 Project Overview

N-Gram Model & POS Tagging is a **Streamlit-based Natural Language Processing (NLP) application** that performs **Unigram, Bigram, and Trigram analysis** along with **Part-of-Speech (POS) tagging** using Rule-Based, Probabilistic, HMM, and Transformer-based approaches.

---

## 🚀 Key Features

* 🔤 **Text Tokenization** using regular expressions
* 1️⃣ **Unigram Analysis** with frequency and probability
* 2️⃣ **Bigram Analysis** with frequency, probability, and next-word prediction
* 3️⃣ **Trigram Analysis** with frequency, probability, and next-word prediction
* 🏷️ **Rule-Based POS Tagging**
* 📊 **Probabilistic POS Tagging** using NLTK
* 🧠 **HMM POS Tagging** using the Brown Corpus
* 🤖 **Transformer-based POS Tagging**
* 🖥️ **Interactive Streamlit UI**

---

## 🛠️ Technologies Used

| Technology       | Purpose                       |
| ---------------- | ----------------------------- |
| **Python**       | Core programming language     |
| **Streamlit**    | User interface                |
| **NLTK**         | POS tagging and Brown Corpus  |
| **Transformers** | Transformer-based POS tagging |
| **PyTorch**      | Transformer model support     |

---

## 📂 Project Structure

```text
NLP_EXP6/
├── app.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### 1. Create a Virtual Environment

```bash
python -m venv .venv
```

### 2. Activate the Virtual Environment

**Windows:**

```bash
.venv\Scripts\activate
```

**macOS/Linux:**

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

Run the following command from the project folder:

```bash
streamlit run app.py
```

The application will open in your default web browser.

---

## 🧠 How It Works

```text
Input Text
    ↓
Tokenization
    ↓
Select POS Tagging Model
    ↓
POS Tagging
    ↓
Select N-Gram Model
    ↓
Generate N-Grams
    ↓
Calculate Frequencies & Probabilities
    ↓
Display Results & Predictions
```

---

## 🏷️ POS Tagging Models

### Rule-Based

Uses predefined linguistic rules and word patterns to assign POS tags such as:

```text
DT, PRP, IN, CC, VB, VBG, VBD, RB, JJ, NN, NNS
```

### Probabilistic

Uses the **NLTK POS tagger** to assign POS tags based on a trained statistical model.

### HMM

Uses a **Hidden Markov Model (HMM)** trained on the **NLTK Brown Corpus** and applies the Viterbi algorithm for POS tagging.

### Transformer

Uses a **pre-trained BERT-based Transformer model** for POS tagging.

---

## 📐 N-Gram Models

### Unigram

A Unigram consists of **one word**.

```text
P(w) = Count(w) / Total Context
```

### Bigram

A Bigram consists of **two consecutive words**.

```text
P(w₂ | w₁) = Count(w₁,w₂) / Count(w₁)
```

### Trigram

A Trigram consists of **three consecutive words**.

```text
P(w₃ | w₁,w₂) = Count(w₁,w₂,w₃) / Count(w₁,w₂)
```

The application uses **Laplace smoothing** when calculating N-gram probabilities.

---

## 🔮 Next-Word Prediction

For Bigram and Trigram models, the application:

1. Takes the last word or last two words as the context.
2. Finds matching N-grams from the input.
3. Calculates their probabilities.
4. Displays the top possible next words.

---

## 🖥️ Application Sections

The Streamlit interface contains:

* **🏷️ POS Tagging** – Displays word-level POS tags and the tagged sentence
* **🔤 N-Gram Analysis** – Displays N-gram frequencies and probabilities
* **🔮 Next-Word Prediction** – Displays possible next words for Bigram and Trigram models

---

## 📥 Output

The application provides:

* POS-tagged words
* Tagged sentences
* Unigram, Bigram, and Trigram frequency tables
* N-gram probabilities
* Next-word predictions
* Results for multiple POS tagging approaches