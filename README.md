# Amazon Review Sentiment Analysis 🛒

## Project Overview 🌟
This project focuses on performing **sentiment analysis** on Amazon product reviews for Kozmos, a company producing home textiles and daily clothing. By analyzing customer reviews, the goal is to extract insights and help the company improve its products and services.

---

## Problem Statement 📝
Amazon reviews contain valuable information about customer satisfaction. The aim of this project is to:  

- 🔹 Analyze review texts  
- 🔹 Label them as positive or negative  
- 🔹 Build machine learning models to classify sentiment  
- 🔹 Provide actionable insights to support business decisions  

---

## Dataset 📦
The dataset consists of 5611 observations and 4 variables:  

| Column    | Description                               |
|-----------|-------------------------------------------|
| Star      | Product rating given by the customer     |
| Helpful   | Number of people who found the review useful |
| Title     | Review title (short comment)             |
| Review    | Full review text                          |

---

## Workflow ⚡

### 1. Data Preprocessing 🧹
- Text cleaning: lowercase conversion, punctuation removal, number removal  
- Stopwords removal  
- Lemmatization to get word roots  

### 2. Word Frequency Analysis 📊
We calculated word frequencies and removed rare words.  

### 3. Sentiment Analysis ❤️/💔
Using **NLTK's SentimentIntensityAnalyzer**, reviews were labeled as positive (`pos`) or negative (`neg`) based on the compound score.  

### 4. Feature Extraction 🔧
- TF-IDF vectorization (1-2 grams, 5000 features)  
- Train-test split (80-20)  

### 5. Machine Learning Models 🤖
We applied and evaluated two models:

| Model                  | Accuracy | Precision | Recall | F1-Score |
|------------------------|----------|-----------|--------|-----------|
| Logistic Regression    | 0.86     | 0.89      | 0.92   | 0.91      |
| Random Forest (CV)     | 0.88     | 0.93      | 0.91   | 0.92      |

- **Observation**: Logistic Regression had a higher recall (better at catching negative reviews), while Random Forest achieved higher precision (fewer false positives).

---

## Conclusion ✅
- The Random Forest model performed best overall.  
- The analysis helps extract insights from Amazon reviews and can guide product improvement strategies.  
- Negative reviews are sometimes misclassified as positive due to dataset imbalance, indicating a bias toward predicting positive sentiment.

---

## Tools & Libraries 🔧
- Python (pandas, numpy, re)  
- NLTK (tokenization, stopwords, lemmatization, SentimentIntensityAnalyzer)  
- Scikit-learn (TF-IDF, Logistic Regression, Random Forest, GridSearchCV)  
- Visualization (matplotlib, seaborn, WordCloud)  

---

## Future Work 🚀
- Balance the dataset to reduce bias in negative review classification  
- Experiment with advanced NLP models like BERT or RoBERTa  
