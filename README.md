# NLP-Text-Preprocessing-and-Lemmatization-with-NLTK

# NLP Text Preprocessing Using NLTK

## 📌 Project Overview
Natural Language Processing (NLP) requires raw text data to be cleaned and normalized before applying machine learning or deep learning models. This project demonstrates a basic NLP preprocessing pipeline using the **NLTK** library in Python.

The project focuses on converting raw text into a cleaned and structured format by applying sentence tokenization, word tokenization, stopword removal, and lemmatization.

---

## 🧠 Key NLP Concepts Covered
- Sentence Tokenization
- Word Tokenization
- Stopword Removal
- Lemmatization
- Text Normalization

---

## 🛠️ Technologies Used
- Python
- NLTK (Natural Language Toolkit)

---

## 📂 Workflow
1. Input raw paragraph text
2. Split text into sentences
3. Tokenize each sentence into words
4. Remove common stopwords
5. Apply lemmatization using WordNet Lemmatizer
6. Reconstruct cleaned sentences

---

## 🧪 Sample Code Explanation

### Importing Required Libraries

import nltk

from nltk.stem import WordNetLemmatizer

from nltk.corpus import stopwords

## Input Text
paragraph = """AI, machine learning and deep learning are common terms in enterprise IT..."""

## Sentence Tokenization
sentence = nltk.sent_tokenize(paragraph)

## Lemmatization & Stopword Removal

stemmer = WordNetLemmatizer()

for i in range(len(sentence)):

    words = nltk.word_tokenize(sentence[i])
    
    words = [stemmer.lemmatize(word) for word in words 
    
             if word not in set(stopwords.words('english'))]
             
    sentence[i] = ' '.join(words)
    

## 📈 Output

Cleaned and normalized sentences

Reduced noise in text

Improved quality of textual data for downstream NLP tasks

## 🎯 Applications

Text Classification

Sentiment Analysis

Document Clustering

Search Engines

Chatbots

## 🚀 Future Enhancements

Stemming vs Lemmatization comparison

POS tagging

TF-IDF and Bag of Words

Named Entity Recognition (NER)
