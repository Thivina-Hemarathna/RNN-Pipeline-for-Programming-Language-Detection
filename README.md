# 🧠 RNN Pipeline for Programming Language Prediction

# 🧠 RNN Pipeline for Programming Language Prediction

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red.svg)](https://pytorch.org/)
[![Course](https://img.shields.io/badge/Course-APS360-orange.svg)](https://engineering.calendar.utoronto.ca/course/aps360h1)
[![Model](https://img.shields.io/badge/Model-RNN%20%7C%20LSTM%20%7C%20GRU-green.svg)](#)


> **APS360 – Applied Fundamentals of Deep Learning**  
> University of Toronto

📌 **Author:** Thivina Suduwa Devage  
📧 **Email:** thivina.suduwadevage@mail.utoronto.ca  
🔗 **Repository:** https://github.com/Thivina-Hemarathna/RNN-Pipeline-for-Programming-Language-Detection

---

## 🚀 Project Overview

Identifying the programming language of a source code snippet is a fundamental problem in software engineering, with applications in code search, repository mining, automated documentation, plagiarism detection, and developer productivity tools.

Traditional approaches based on file extensions or keyword matching often fail when dealing with short, incomplete, or noisy code snippets commonly found in forums, logs, and student submissions.

This project presents a **Recurrent Neural Network (RNN)–based pipeline** that predicts the programming language of a code snippet directly from its raw textual representation, without relying on handcrafted rules.

---

## 🧩 Key Idea

Programming languages exhibit strong sequential structure, including:

- Keyword ordering  
- Punctuation and symbol usage  
- Indentation and formatting patterns  

By modeling code as a **sequence of characters or tokens**, an RNN can learn language-specific syntactic and stylistic patterns and generalize effectively across snippets of varying length.

---

## 🏗️ System Architecture

<p align="center">
  <img src="/Project Proposal/RNN_layout.png" alt="RNN Pipeline Diagram" width="650"/>
</p>

**Pipeline Stages:**

1. Raw source code snippet input  
2. Preprocessing and normalization  
3. Character-level or token-level embedding  
4. RNN encoder (LSTM or GRU)  
5. Fully connected classification layer  
6. Softmax output over programming languages  

---

## 📂 Dataset & Preprocessing

### Data Sources
- Public GitHub repositories  
- Curated datasets such as **CodeSearchNet**

### Preprocessing Steps
- Removal of comments (where appropriate)
- Whitespace normalization
- Filtering extremely short or non-informative snippets
- Optional character-level or token-level representation

The dataset is split into **training**, **validation**, and **test** sets.

---

## 🤖 Model Design

### Core Model
- Recurrent Neural Network (RNN)
- LSTM or GRU cells
- Final hidden state used as a fixed-length representation of the code snippet

### Output Layer
- Fully connected layer
- Softmax activation for multi-class classification

---

## 📉 Baseline Model

To provide a meaningful comparison, a traditional machine learning baseline is implemented using:

- Character-level n-gram features  
- Multinomial Naive Bayes or Support Vector Machine (SVM)

This baseline serves as a strong reference point for evaluating the performance of the RNN-based approach.

---

## 📈 Evaluation Metrics

Model performance is evaluated using:

- Classification accuracy  
- Confusion matrix  
- Per-language precision and recall  

Performance comparisons are made between classical baselines and deep learning models.

---

## ⚖️ Ethical Considerations

- All data is sourced from publicly available repositories
- Licensing terms are respected
- Potential dataset bias is acknowledged
- Model predictions should not be used as the sole basis for plagiarism accusations or automated grading without human oversight

---

## 🛠️ Technologies Used

- Python  
- PyTorch  
- NumPy  
- Pandas  
- Scikit-learn  
- Git & GitHub  

---

## 🎯 Project Goals

- Build a robust RNN-based programming language classifier  
- Compare deep learning models with classical baselines  
- Understand how sequential models capture syntactic patterns in code  
- Deliver a clean, interpretable, and reproducible ML pipeline  

---

## 📌 Course Context

This project was completed as part of **APS360: Applied Fundamentals of Deep Learning** at the **University of Toronto**.

---

## 🌟 Future Work

- Extend to additional programming languages  
- Experiment with bidirectional RNNs  
- Compare against transformer-based models (e.g., CodeBERT)  
- Incorporate syntax-aware tokenization methods  

---
