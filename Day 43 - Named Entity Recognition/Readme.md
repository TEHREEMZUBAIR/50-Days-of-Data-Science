
# 📄 Day 43: Named Entity Recognition 🧠

## Task Overview
Welcome to **Day 43** of your data science journey! 🚀 Today’s task is centered on **Sentiment Analysis** 📝. We will be using natural language processing (NLP) techniques to classify text data into various sentiment categories such as *Positive*, *Neutral*, or *Negative*.

---

## 🛠️ Prerequisites
Before getting started, make sure you have the following libraries installed:
1. **Python 3.x** 🐍
2. **Jupyter Notebook** (for running the notebook)
3. **NLTK** (Natural Language Toolkit)
   - Install using: `pip install nltk`
4. **Pandas** (for data manipulation)
   - Install using: `pip install pandas`
5. **scikit-learn** (for building the classification model)
   - Install using: `pip install scikit-learn`

---

## 📂 File Structure
- `task-43.ipynb` - Main notebook containing code for text preprocessing and sentiment analysis.
- **Dataset:** A sample dataset containing text entries with sentiment labels.

---

## 🔄 Instructions

1. **Data Loading and Exploration** 📊
   First, load the dataset and explore its structure. The dataset should contain columns for the text data and corresponding sentiment labels.
   ```python
   import pandas as pd
   data = pd.read_csv('your_dataset.csv')
   data.head()
   ```

2. **Text Preprocessing Steps** 🧹
   - **Tokenization:** Split the text into individual tokens (words).
   - **Lowercase Conversion:** Convert all text to lowercase to ensure uniformity.
   - **Stopword Removal:** Eliminate common stopwords like 'the', 'and', etc.
   - **Short Word Removal:** Remove words with less than 3 characters.
   - **Cleaning Symbols:** Remove symbols, hashtags, mentions, and hyperlinks.

   Here’s a sample of how the preprocessing can be done:
   ```python
   import re
   import nltk
   nltk.download('stopwords')
   from nltk.corpus import stopwords

   def clean_text(text):
       text = re.sub(r"@\w+|https?://\S+|#\w+|RT", "", text)  # Remove mentions, links, hashtags, RT
       text = re.sub(r"[^a-zA-Z\s]", "", text)  # Remove non-alphabetic characters
       tokens = text.lower().split()  # Convert to lowercase and tokenize
       tokens = [word for word in tokens if word not in stopwords.words('english') and len(word) > 2]
       return " ".join(tokens)
   
   data['cleaned_text'] = data['text_column'].apply(clean_text)
   ```

3. **Sentiment Labeling** 😊😐😡
   Assign labels to each text entry according to the sentiment category (Positive, Neutral, or Negative).
   ```python
   data['sentiment'] = data['sentiment_column'].map({0: 'Negative', 1: 'Neutral', 2: 'Positive'})
   ```

4. **Train-Test Split** 📚
   Split the dataset into training and testing sets for building and evaluating the model.
   ```python
   from sklearn.model_selection import train_test_split
   X_train, X_test, y_train, y_test = train_test_split(data['cleaned_text'], data['sentiment'], test_size=0.2)
   ```

5. **Model Building** 🤖
   Use a **Machine Learning Model** like a Logistic Regression classifier or any other model for sentiment classification:
   ```python
   from sklearn.feature_extraction.text import TfidfVectorizer
   from sklearn.linear_model import LogisticRegression

   # Convert text to numerical features using TF-IDF
   vectorizer = TfidfVectorizer()
   X_train_vec = vectorizer.fit_transform(X_train)
   X_test_vec = vectorizer.transform(X_test)

   # Train Logistic Regression model
   model = LogisticRegression()
   model.fit(X_train_vec, y_train)
   ```

6. **Model Evaluation** 📉
   Evaluate the performance of your model using accuracy, precision, recall, and F1-score.
   ```python
   from sklearn.metrics import classification_report
   y_pred = model.predict(X_test_vec)
   print(classification_report(y_test, y_pred))
   ```

---

## 🎯 Task Objectives
- Preprocess text data to clean, tokenize, and label sentiments.
- Build and train a sentiment classification model using machine learning.
- Evaluate the model's performance on test data.

---

## 🧪 Additional Experiments
- Try different models like **Naive Bayes** or **SVM** to see if they improve performance.
- Experiment with hyperparameters of the **TF-IDF vectorizer** (e.g., `ngram_range`, `max_features`) to improve feature extraction.

---

## 💡 Tips
- Preprocessing is crucial for text data. Make sure to experiment with various cleaning methods for better results.
- Pay close attention to **class imbalance**. If one sentiment is heavily dominant, consider balancing the dataset.

---

## 📚 Resources
- [NLTK Documentation](https://www.nltk.org/)
- [Scikit-learn Documentation](https://scikit-learn.org/)

---

Happy coding! 💻✨

---