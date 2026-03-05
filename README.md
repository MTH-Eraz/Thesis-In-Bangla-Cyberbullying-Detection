# Bangla Cyberbullying Detection using Transformer-Based Models

## Overview
Cyberbullying has become a serious issue on social media platforms, particularly in user-generated content environments. Detecting abusive or harmful comments automatically is crucial for improving online safety.

This research project focuses on detecting **Bangla cyberbullying comments** using **Natural Language Processing (NLP)** and **Transformer-based models**. The study compares classical machine learning models with modern transformer architectures and introduces an **ensemble model** to improve classification performance.

The final system achieves **92.20% accuracy** using a soft-voting ensemble of **BERT and XLM-RoBERTa**.

---

## Problem Statement
Detecting cyberbullying in Bangla text presents several challenges:

- Informal social media language
- Spelling variations and slang
- Dialectal expressions
- Code-mixed Bangla–English text
- Context-dependent abusive expressions

Most existing cyberbullying detection systems focus on **English datasets**, while **Bangla datasets remain limited**. This project addresses that gap.

---

## Dataset

The dataset used in this research was constructed through a multi-stage pipeline to ensure label consistency and experimental reliability.

### Dataset Pipeline

44k Category Dataset  
↓  
18k Binary Dataset  
↓  
18k Converted Category Dataset  
↓  
Final Dataset (60,153 samples)

### Dataset Categories

| Label | Category |
|------|---------|
|0|Not Bully|
|1|Threat|
|2|Religious|
|3|Troll|
|4|Sexual|

The final dataset contains **60,153 Bangla social media comments**.

---

## Data Preprocessing

The following preprocessing steps were applied:

- Lowercasing
- Special character removal
- Duplicate removal
- Tokenization
- Label encoding
- Dataset splitting

Transformer models used **minimal preprocessing** to preserve contextual information.

---

## Models Used

This research evaluates multiple approaches:

### 1️⃣ Classical Machine Learning

- TF-IDF Feature Extraction
- Linear Support Vector Machine
- Logistic Regression

A **two-stage classification pipeline** was implemented:
- Binary classification (Bully vs Not Bully)
- Multi-class classification (Cyberbullying categories)

---

### 2️⃣ Transformer Models

#### BERT
A pretrained transformer model capable of generating contextual embeddings for text.

#### XLM-RoBERTa
A multilingual transformer model that improves cross-lingual understanding and performs better for minority classes.

---

### 3️⃣ Ensemble Model

To improve prediction stability and accuracy, a **soft voting ensemble** was implemented.

The ensemble combines probability outputs from BERT and XLM-R:
