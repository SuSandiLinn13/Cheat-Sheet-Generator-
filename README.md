# Cheat-Sheet Generator  
### Hybrid Extractive Text Summarization using BERT + TF-IDF + Logistic Regression

## Project Overview
This project implements a **Hybrid Extractive Summarization System** that automatically generates concise cheat-sheets from lecture PDFs and academic text documents.

The system combines **deep contextual understanding from BERT** with **statistical feature-based sentence classification using TF-IDF and Logistic Regression** to improve summary quality and relevance.

This hybrid approach helps capture both:
- Semantic importance of sentences
- Keyword-based statistical significance

---
## Kaggle Notebook

You can explore the full implementation and run the hybrid summarization pipeline on Kaggle:

🔗 **Hybrid Extractive Text Summarizer Notebook**  
https://www.kaggle.com/code/susandilinn/hybrid-text-summarizer

---
## Model Architecture

The summarization pipeline consists of three major components:

### BERT Model (`bert_model`)
- Pretrained **BERT-base-uncased**
- Generates contextual sentence embeddings
- Captures semantic meaning and concept relationships
- Helps identify conceptually important sentences

### TF-IDF Vectorizer (`tfidf_vectorizer`)
- Converts sentences into numerical feature vectors
- Measures importance of words based on document frequency
- Highlights domain-specific and technical terms

### Logistic Regression Classifier (`logistic_model`)
- Supervised model trained to classify whether a sentence should be included in the summary
- Uses TF-IDF features and semantic signals
- Outputs probability scores for sentence selection

---

## System Workflow

1. Combine multiple lecture PDFs  
2. Extract raw text content  
3. Perform sentence tokenization  
4. Generate TF-IDF feature vectors  
5. Compute BERT sentence embeddings  
6. Logistic Regression predicts sentence importance  
7. Selected sentences are merged to generate the final cheat-sheet  

---
## Notebooks Description

This project contains several Jupyter notebooks that implement different stages of the hybrid summarization pipeline.

### pdf_combination.ipynb
- Combines multiple lecture PDF files into a single document  
- Performs initial text extraction and preprocessing  

### extractive-summarizer-bert-based-uncased.ipynb
- Uses pretrained BERT model to generate contextual sentence embeddings  
- Computes semantic importance scores for each sentence  

### Logistic_regression_cheetaxh.ipynb
- Trains the Logistic Regression classifier  
- Uses TF-IDF features to learn sentence importance  
- Saves the trained model (`logistic_model.pkl`)  

### hybrid-extrative-text-summarizer.ipynb
- Main notebook implementing the hybrid summarization pipeline  
- Combines BERT semantic scores with Logistic Regression predictions  
- Generates the final cheat-sheet summary  

### extracted_equations.ipynb
- Extracts equations from lecture materials  
- Converts detected equations into LaTeX format for structured notes  

---

## Key Features

- Hybrid Deep Learning + Machine Learning approach  
- Designed for lecture notes and academic materials  
- Improves summary relevance and information density  
- Modular architecture for easy experimentation  
- Automatic cheat-sheet generation pipeline  

---

## Tech Stack

- Python  
- Scikit-learn  
- HuggingFace Transformers  
- NLTK / SpaCy  
- NumPy  
- Pandas  

---
