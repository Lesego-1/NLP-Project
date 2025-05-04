# 🧠 Customer Feedback Sentiment Analysis

## 📌 Project Overview

In today's data-driven world, businesses receive vast amounts of unstructured feedback from customers across channels like emails, social media, surveys, and product reviews. Manually processing this feedback is time-consuming and inefficient. This project applies **Natural Language Processing (NLP)** to automate the classification of customer feedback sentiment, enabling businesses to identify key issues, prioritize improvements, and enhance customer satisfaction.

---

## 🎯 Problem Statement

The primary objective is to build a model that can:

- Automatically classify customer feedback as **positive** or **negative** based on sentiment.
- Perform **Aspect-Based Sentiment Analysis (ABSA)** to extract specific product or service aspects mentioned in the feedback, identify the associated opinion, and determine the sentiment polarity (positive/negative).

---

## ⚙️ Methodology

The sentiment analysis pipeline consists of the following steps:

1. **Data Loading**  
   Import and structure customer feedback data with review ratings used to define sentiment labels.

2. **Data Balancing**  
   Apply **oversampling techniques** to ensure a balanced distribution of sentiment classes.

3. **Language Filtering**  
   Filter feedback to **English-only** entries for consistent processing.

4. **Text Cleaning**  
   Use **regular expressions** to remove unwanted characters, symbols, and formatting.

5. **Tokenization**  
   Split text into individual tokens (words) for further processing.

6. **Stop Word Removal**  
   Eliminate commonly used words (e.g., *the*, *is*, *and*) that do not carry sentiment.

7. **Lemmatization**  
   Reduce words to their base form (e.g., *running* → *run*) to normalize the data.

8. **Vectorization**  
   Convert cleaned text into numerical features suitable for model input using embedding or vectorization techniques.

9. **Model Training**  
   Train a **Long Short-Term Memory (LSTM)** neural network for binary sentiment classification.

10. **Prediction & Evaluation**  
    Generate predictions and evaluate model performance using accuracy and confusion matrices.

---

## 📊 Results

### ✅ Sentiment Classification

- The **LSTM model** achieved an **accuracy of 84%** on the test data.
- This performance is expected to **scale positively** with larger, more diverse datasets.
- The model effectively distinguishes between positive and negative sentiments, offering a practical solution for monitoring brand perception and identifying dissatisfied customers.

### 🧩 Aspect-Based Sentiment Analysis (ABSA)

- The ABSA module successfully returns:
  - The **aspect** (e.g., "battery life")
  - The **opinion phrase** (e.g., "very poor")
  - The **sentiment** of the opinion (e.g., "negative")
- This granularity provides actionable insights by highlighting which **specific features** are praised or criticized.
- Businesses can use these insights to improve products, prioritize feature updates, and tailor customer support strategies.

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- SpaCy
- Keras
- Scikit-learn
- Seaborn / Matplotlib