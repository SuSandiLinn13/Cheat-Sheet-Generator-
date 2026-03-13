# Cheat-Sheet Generator  
### Hybrid Extractive Text Summarization using BERT + TF-IDF + Logistic Regression

## Project Overview
This project implements a **Hybrid Extractive Summarization System** that automatically generates concise cheat-sheets from lecture PDFs and academic text documents.

The system combines **deep contextual understanding from BERT** with **statistical feature-based sentence classification using TF-IDF and Logistic Regression** to improve summary quality and relevance.

This hybrid approach helps capture both:
- Semantic importance of sentences
- Keyword-based statistical significance

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

## Project Structure
Cheat-Sheet-Generator/
│
├── model/
│ ├── bert_model/ # Saved pretrained BERT model
│ ├── logistic_model.pkl # Trained Logistic Regression classifier
│ └── tfidf_vectorizer.pkl # Fitted TF-IDF vectorizer
│
├── extractive-summarizer-bert-based-uncased.ipynb # BERT sentence embedding & scoring
├── hybrid-extrative-text-summarizer.ipynb # Final hybrid summarization pipeline
├── Logistic_regression_cheetaxh.ipynb # Logistic Regression training
├── pdf_combination.ipynb # Combine lecture PDFs
├── extracted_equations.ipynb # Equation extraction & LaTeX conversion
│
└── README.md
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
