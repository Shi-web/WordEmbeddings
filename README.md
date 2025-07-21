# Word2Vec for Spam Email Classification

## Overview

This is a demo lab from Break Through Tech's AI Program. This demo demonstrates how to use Word2Vec embeddings to build a spam email classifier. Unlike traditional bag-of-words approaches, Word2Vec captures semantic relationships between words, potentially improving classification accuracy by understanding context and meaning rather than just word frequency.

## Learning Objectives

- How to train domain-specific Word2Vec models using Gensim
- The importance of training embeddings on relevant text corpora
- How to convert word embeddings into document-level feature vectors
- How to integrate Word2Vec features with traditional machine learning classifiers
- Text preprocessing techniques for NLP tasks
- End-to-end pipeline for text classification projects

## Project Workflow

### 1. Data Loading
- Import spam email dataset containing email subject lines
- Examine dataset structure and distribution of spam vs. legitimate emails

### 2. Data Preparation
- Create labeled examples with text features (subject lines) and binary labels (spam/not spam)
- Structure data for machine learning pipeline

### 3. Text Preprocessing
- Convert text to lowercase for consistency
- Remove punctuation and special characters
- Filter out stop words (common words like "the", "and", "is")
- Clean and normalize text data

### 4. Dataset Splitting
- Create training and test datasets
- Ensure proper separation for unbiased model evaluation
- Each example contains one preprocessed email subject line

### 5. Word2Vec Model Training
- Train Word2Vec model using Gensim on the training corpus
- Learn vector representations based on word co-occurrence patterns
- Inspect resulting embeddings to understand semantic relationships
- Explore similar words and word analogies

### 6. Feature Vector Creation
- Convert each email subject line into a numerical feature vector
- Average Word2Vec embeddings of all words in each subject line
- Handle out-of-vocabulary words appropriately
- Create consistent-length feature vectors for machine learning

### 7. Classification Model Training
- Train logistic regression classifier using Word2Vec-derived features
- Evaluate model performance on test dataset
- Compare results with baseline approaches
- Analyze classification accuracy and potential improvements

## Key Concepts

### Domain Relevance
**Critical Insight**: Word2Vec models should be trained on text from the same domain as your target application. Training on medical texts for a finance application would be suboptimal because the semantic relationships learned would be irrelevant to the target domain.

### Feature Vector Construction
Rather than using individual word embeddings, we create document-level representations by averaging all word vectors in each email subject line. This provides a fixed-length feature vector suitable for traditional machine learning algorithms.

### Word2Vec Advantages
- Captures semantic relationships between words
- Handles synonyms and related terms effectively
- Provides dense, meaningful representations vs. sparse bag-of-words
- Enables transfer of learning across similar words

## Technologies Used

- **Python**: Primary programming language
- **Gensim**: Word2Vec model training and word embedding generation
- **scikit-learn**: Logistic regression classifier and evaluation metrics
- **pandas/numpy**: Data manipulation and numerical operations
- **NLTK/spaCy**: Text preprocessing and natural language processing

## Expected Outcomes

Upon completion, you will have:
- A trained Word2Vec model specific to email/spam domain
- Understanding of how semantic embeddings improve text classification
- Practical experience with end-to-end NLP pipeline development
- Insights into the relationship between domain-specific training and model performance
- A working spam classifier that can predict whether new emails are spam

## Prerequisites

- Basic Python programming knowledge
- Understanding of machine learning classification concepts
- Familiarity with text preprocessing concepts
- Basic knowledge of logistic regression


This project provides hands-on experience with modern NLP techniques and demonstrates how semantic word embeddings can enhance traditional machine learning approaches for text classification tasks.
