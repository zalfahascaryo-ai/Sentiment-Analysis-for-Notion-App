# Sentiment-Analysis-for-Notion-App

## 🔎 Project Overview
This project focuses on analyzing user sentiment from reviews of the Notion app collected from the Google Play Store. By leveraging Natural Language Processing (NLP) techniques, the system processes raw textual data and classifies user opinions into sentiment categories.

The project implements a complete end-to-end pipeline, starting from manual data collection to model evaluation, combining multiple feature extraction techniques with both machine learning and deep learning models. The goal is to explore different approaches and identify the most effective method for sentiment classification.

## ⚙️ Project Pipeline
### 1. Data Collection: 
The dataset is manually scraped from the Google Play Store using the `google_play_scraper` library

### 2. Data preprocessing: 
* Cleaning text: Remove non-alphabet characters
* Casefolding text: Convert all text to lowercase
* Fix slangwords: Replace slang words or acronyms with standard forms
* Tokenizing text: Split sentences into individual words
* Filtering text: Remove common words that do not add significant meaning
* Negation handling: Transform phrases like “*not good*” → “*bad*”
* Lemmatize token: Normalize words using Part-of-Speech (POS) tagging for better accuracy

### 3. Feature Extraction:
  * TF-IDF: Converts text into weighted numerical vectors based on word importance
  * Count: Represents text using word frequency
  * Numerical features: Incorporates features such as `thumbsUpCount` and `score`, combined with text features
 
### 4. Model Development: 
* Machine learning models: 
  - Logistic Regression
  - Support Vector Machine (SVM)
  These models are chosen because they are well-known for strong performance in text classification tasks, especially when combined with TF-IDF features. They are also efficient, interpretable, and suitable as baseline models.
  
* Deep learning models: 
  - Multi Layer Perceptron (MLP)
  MLP is used to capture more complex patterns in the data compared to traditional machine learning models. It allows the model to learn non-linear relationships between features and improve classification performance.
  
### 5.  Model Evaluation:
The model is evaluated by the precision, recall, and f-1 score. A confusion matrix is also provided to give a detailed view of prediction performance across each sentiment class.

## ✨ Future Work
There were a lot of imrovement for this project:
* Replace manual scraping with automated pipelines for continuous data collection
* Implement transformer-based models such as BERT for better contextual understanding
* Build a simple web application (e.g., using Streamlit) to enable real-time sentiment analysis
