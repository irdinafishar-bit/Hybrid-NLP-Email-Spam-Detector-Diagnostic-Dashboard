# hybrid-nlp-email-spam-detector
End-to-end NLP email spam classifier &amp; interactive Streamlit diagnostic app. Engineered a 1,301D hybrid feature space combining TF-IDF, 300D spaCy word embeddings, and WordNet lexical diversity, achieving 96.66% accuracy (97% spam precision) with Random Forest.

# Hybrid Email Spam Classifier & Real-Time Diagnostic Dashboard

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![NLP](https://img.shields.io/badge/NLP-spaCy%20%7C%20NLTK-green)
![Frontend](https://img.shields.io/badge/Frontend-Streamlit-red)

## Overview
An end-to-end Natural Language Processing (NLP) classification pipeline and interactive Streamlit web application designed to detect spam emails with high precision. Rather than relying solely on bag-of-words frequencies, this system fuses statistical n-grams, dense semantic word vectors, and linguistic richness metrics into a unified hybrid feature space.

## Key Features & Architecture
* **Text Preprocessing:** Automated HTML/URL stripping, tokenization, stopword filtering, and lemmatization.
* **1,301-Dimensional Hybrid Feature Engineering:**
  * **Statistical Representation (1,000D):** TF-IDF vectorization capturing high-signal spam keywords and n-gram patterns.
  * **Semantic Representation (300D):** Dense document embeddings generated via `spaCy` (`en_core_web_md`) to capture contextual meaning.
  * **Linguistic Complexity (1D):** Custom WordNet-based lexical diversity metric measuring vocabulary richness.
* **Model Performance:** Evaluated multiple classifiers across the hybrid feature matrix, with **Random Forest** achieving **96.66% overall accuracy** and **97% spam precision**.
* **Interactive Streamlit Diagnostic App:** Allows users to input raw email text for real-time spam probability scoring, confidence breakdowns, and feature diagnostics.

## Tech Stack
* **NLP & Feature Engineering:** `spacy`, `nltk` (WordNet), `scikit-learn` (`TfidfVectorizer`)
* **Modeling & Deployment:** `scikit-learn` (Random Forest), `pandas`, `numpy`, `streamlit`
