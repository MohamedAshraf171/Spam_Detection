# 📧 Spam Detection with Naive Bayes

This project demonstrates a simple yet effective **Spam Email Classifier** built using **Python**, **scikit-learn**, and **Natural Language Processing (NLP)** techniques. It classifies messages as spam or not spam using a **Naive Bayes model** trained on text data.

## 🔍 Overview

The goal is to build a spam detection model that:
- Preprocesses textual message data.
- Converts messages into numerical vectors using **CountVectorizer**.
- Trains a **Multinomial Naive Bayes classifier**.
- Predicts and evaluates the model on unseen data.

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- scikit-learn (Naive Bayes, CountVectorizer, Pipeline, train_test_split)

## 📁 Dataset

The dataset used is `spam.csv`, which contains labeled SMS messages.  
- `Category`: Label indicating spam or ham.
- `Message`: The content of the SMS.

> Ensure the dataset is correctly loaded using `pd.read_csv('/content/spam.csv')`. Adjust the path as needed.

## 🧪 How It Works

1. **Load and Clean Data**:
   - Remove missing values.
   - Convert categories to binary labels (`spam` = 1, `ham` = 0).

2. **Train-Test Split**:
   - Split the dataset into training (70%) and testing (30%) sets.

3. **Build the Pipeline**:
   - Use `CountVectorizer` to convert text to numerical features.
   - Train a `MultinomialNB` classifier.

4. **Model Prediction and Evaluation**:
   - Predict new email samples.
   - Evaluate accuracy on the test set.

## 🧠 Sample Predictions

```python
emails = [
    "Sounds great! Are you home now?",
    "Will u meet ur dream partner soon? Is ur career off 2 a flyng start? To find out free, txt HORO followed by ur star sign, e.g. HORO ARIES"
]

predictions = clf.predict(emails)
print(predictions)  # Output: [0, 1] — First is ham, second is spam
