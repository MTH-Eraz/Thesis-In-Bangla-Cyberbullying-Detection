# Bangla Cyberbullying Detection using Transformer-Based Models

<p align="center">
AI-based detection of abusive Bangla social media comments using NLP and Transformer models
</p>

<p align="center">
<img src="https://img.shields.io/badge/Language-Python-blue?style=for-the-badge">
<img src="https://img.shields.io/badge/NLP-Transformer-green?style=for-the-badge">
<img src="https://img.shields.io/badge/Framework-PyTorch-red?style=for-the-badge">
<img src="https://img.shields.io/badge/Model-BERT%20%7C%20XLMR-purple?style=for-the-badge">
<img src="https://img.shields.io/badge/Accuracy-92.20%25-brightgreen?style=for-the-badge">
</p>

---

# Project Overview

Cyberbullying has become a serious issue across modern social media platforms. Harmful comments and abusive language can negatively impact individuals and communities. Detecting such content manually is difficult due to the massive volume of online communication.

This research project focuses on detecting **Bangla cyberbullying comments** using **Natural Language Processing (NLP)** and **Transformer-based deep learning models**.

The project compares **classical machine learning models** with **state-of-the-art transformer architectures**, and introduces an **ensemble approach** that significantly improves classification performance.

The final ensemble system achieves **92.20% accuracy** for Bangla cyberbullying detection.

---

# Problem Statement

Detecting cyberbullying in Bangla social media text is challenging due to several linguistic and contextual factors:

• Informal language usage  
• Slang and dialect variations  
• Code-mixed Bangla–English text  
• Spelling variations  
• Context-dependent abusive expressions  

Most existing cyberbullying detection systems focus on **English datasets**, while research for **Bangla cyberbullying detection remains limited**.

This project aims to address this gap.

---

# Dataset Construction

A multi-stage dataset construction pipeline was used to ensure label consistency and experimental reliability.

### Dataset Pipeline

44k Category Dataset  
↓  
18k Binary Dataset  
↓  
18k Converted Category Dataset  
↓  
Final Dataset (60,153 Samples)

The final dataset contains **60,153 Bangla social media comments** labeled into cyberbullying categories.

---

# Dataset Categories

| Label | Category |
|------|----------|
| 0 | Not Bully |
| 1 | Threat |
| 2 | Religious |
| 3 | Troll |
| 4 | Sexual |

The dataset includes realistic Bangla social media language patterns such as slang, dialectal expressions, and code-mixed text.

---

# Data Preprocessing

To prepare the dataset for machine learning and transformer models, several preprocessing steps were applied.

• Lowercase normalization  
• Special character removal  
• Duplicate removal  
• Tokenization  
• Label encoding  
• Dataset splitting  

For transformer-based models, **minimal preprocessing** was applied to preserve contextual information.

---

# Models Used

This research evaluates multiple machine learning and deep learning approaches.

---

## Classical Machine Learning

Traditional NLP models were used as a baseline.

Algorithms used:

• TF-IDF Feature Extraction  
• Linear Support Vector Machine  
• Logistic Regression  

A **two-stage classification pipeline** was implemented:

Stage 1 → Binary Classification (Bully vs Not Bully)  
Stage 2 → Multi-Class Classification (Cyberbullying categories)

---

## Transformer Models

### BERT

Bidirectional Encoder Representations from Transformers (BERT) generates contextual word embeddings that capture semantic relationships within text.

Key advantages:

• Contextual word representation  
• Pretrained language knowledge  
• Strong NLP performance

---

### XLM-RoBERTa

XLM-RoBERTa is a multilingual transformer model trained on large cross-lingual corpora.

Advantages:

• Multilingual contextual understanding  
• Better performance for low-resource languages  
• Improved minority class detection

---

## Ensemble Model

To improve classification accuracy and stability, a **soft voting ensemble model** was implemented.

The ensemble combines probability outputs from BERT and XLM-R.


Optimal weights:

BERT = 0.475  
XLM-R = 0.525  

The ensemble model leverages the strengths of both transformer architectures.

---

# Model Performance

| Model | Accuracy |
|------|----------|
| Classical (Binary Stage) | 75.94% |
| Classical (Multi-Class Stage) | 57.44% |
| BERT | 82.47% |
| XLM-R | 84.25% |
| Ensemble | **92.20%** |

Transformer-based models significantly outperform classical machine learning approaches.

The ensemble model achieves the **highest accuracy and best overall performance**.

---

# Real-Time Demonstration

A real-time cyberbullying detection interface was implemented using **Streamlit**.

### Real-Time Workflow

1. User inputs Bangla text  
2. Text is tokenized using pretrained tokenizer  
3. BERT and XLM-R generate prediction probabilities  
4. Ensemble model calculates final prediction  
5. System returns the predicted category

This demonstrates the **practical deployment capability of the proposed system**.

---

# Technologies Used

| Technology | Purpose |
|-----------|--------|
| Python | Programming language |
| PyTorch | Deep learning framework |
| HuggingFace Transformers | Transformer model implementation |
| Scikit-learn | Classical ML models |
| Pandas | Data processing |
| NumPy | Numerical computation |
| Matplotlib | Visualization |
| Streamlit | Real-time application interface |

---

# Project Structure

bangla-cyberbullying-detection  
│  
├── dataset  
├── models  
├── notebooks  
├── figures  
├── tables  
├── streamlit_app  
├── training_scripts  
└── README.md  

---

# Future Work

Future improvements for this research may include:

• Expanding the Bangla cyberbullying dataset  
• Exploring advanced transformer architectures  
• Multimodal cyberbullying detection (text + image)  
• Integration with real social media moderation systems  

---

# Author

Tamjidul Hasan  

Research Interests:

• Natural Language Processing  
• Machine Learning  
• Cyberbullying Detection  

---

# License

This project is intended for **academic and research purposes**.
