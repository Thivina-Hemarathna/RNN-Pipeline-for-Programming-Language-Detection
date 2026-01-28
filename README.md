🧠 RNN Pipeline for Programming Language Prediction

APS360 – Applied Fundamentals of Deep Learning
University of Toronto

📌 Author: Thivina Suduwa Devage
📧 Email: thivina.suduwadevage@mail.utoronto.ca

🔗 Repository: RNN-Pipeline-for-Programming-Language-Detection

🚀 Project Overview

Identifying the programming language of a source code snippet is a fundamental problem in software engineering, with applications in:

🔍 Code search & repository mining

📚 Automated documentation & syntax highlighting

🧪 Plagiarism detection & educational tooling

⚙️ Developer productivity tools

While traditional approaches rely on file extensions or keyword matching, they often fail when faced with short, incomplete, or noisy code snippets—common in forums, logs, and student submissions.

This project introduces a Recurrent Neural Network (RNN)–based pipeline that predicts the programming language of a code snippet directly from raw text, without relying on handcrafted rules.

🧩 Key Idea

Programming languages exhibit strong sequential patterns, such as:

Keyword ordering

Punctuation and symbols

Indentation and formatting styles

By modeling code as a sequence of characters or tokens, an RNN can learn these patterns and distinguish between languages effectively.

🏗️ System Architecture
<p align="center"> <img src="rnn_pipeline.png" alt="RNN Pipeline Diagram" width="650"/> </p>

Pipeline Stages:

Input: Raw source code snippets

Preprocessing: Cleaning, normalization, and filtering

Embedding Layer: Converts characters/tokens into dense vectors

RNN Encoder: LSTM or GRU captures sequential dependencies

Classifier: Fully connected layer with softmax output

Prediction: Programming language probabilities

📂 Dataset & Preprocessing
📊 Data Sources

Public GitHub repositories

Curated datasets such as CodeSearchNet

🛠️ Preprocessing Steps

Removal of comments (where appropriate)

Whitespace normalization

Filtering extremely short or non-informative snippets

Optional character-level or token-level representation

The dataset is split into:

Training

Validation

Test sets

🤖 Model Design
🔹 Core Model

Recurrent Neural Network (RNN)

LSTM or GRU cells

Learns long-range dependencies in code sequences

Final hidden state used as a fixed-length representation

🔹 Output Layer

Fully connected layer

Softmax activation over programming language classes

📉 Baseline Comparison

To evaluate the effectiveness of the RNN model, a baseline classifier is implemented using:

Character-level n-gram features

Naive Bayes or Support Vector Machine (SVM)

This provides a strong, interpretable reference point against which deep learning performance is measured.

📈 Evaluation Metrics

Model performance is assessed using:

✅ Classification Accuracy

📊 Confusion Matrix

🔁 Per-language Precision & Recall

Comparisons are made between:

Baseline ML models

RNN-based deep learning models

⚖️ Ethical Considerations

All data is sourced from public repositories

Licensing terms are respected

Potential dataset bias (e.g., over-representation of popular languages) is acknowledged

The model should not be used as a sole authority for plagiarism detection or grading decisions

📚 Related Work

This project builds upon established research in programming language identification, including:

N-gram and classical ML methods

Character-level RNNs for code classification

Neural language models for source code

Comparisons with transformer-based models (e.g., CodeBERT)

A full list of references is available in the accompanying report.

🛠️ Technologies Used

Python

PyTorch

NumPy / Pandas

Scikit-learn

Git & GitHub

🎯 Project Goals

✔ Build a robust RNN-based classifier for code snippets
✔ Compare deep learning against classical baselines
✔ Understand how sequential models capture code syntax
✔ Deliver a clean, interpretable, and reproducible pipeline

📌 Course Context

This project is completed as part of APS360: Applied Fundamentals of Deep Learning at the University of Toronto, emphasizing:

End-to-end ML pipelines

Model evaluation & comparison

Ethical considerations in AI

🌟 Future Work

Extend to more programming languages

Experiment with bidirectional RNNs

Compare against transformer-based models

Incorporate syntax-aware tokenization
