# 📄 Day 42: Text Processing in NLP 🧠

## Task Overview
Welcome to **Day 42** of your data science journey! 🚀 Today’s focus is on **Lemmatization** in Natural Language Processing (NLP). Lemmatization helps in transforming different forms of a word into its base or root form, known as the *lemma*. Unlike stemming, lemmatization considers the context of the word, making it more accurate for language processing tasks.

---

## 🛠️ Prerequisites
Before diving into the code, ensure you have the following tools and libraries installed:
1. **Python 3.x** 🐍
2. **Jupyter Notebook** (for running the notebook)
3. **spaCy** – NLP library
   - Install it using: `pip install spacy`
4. **NLTK** – Natural Language Toolkit
   - Install it using: `pip install nltk`
5. **WordNet Lemmatizer** (if using NLTK)
   - Install WordNet data: `import nltk; nltk.download('wordnet')`
6. **spaCy Model** – Load the small English model
   - Run: `python -m spacy download en_core_web_sm`

---

## 📂 File Structure
- `task-42.ipynb` - Main notebook for the Lemmatization task.
- Sample text for lemmatization: `"The quick brown foxes are jumping over the lazy dogs."`

---

## 🔄 Instructions

1. **Load the spaCy Model**
   ```python
   import spacy
   nlp = spacy.load('en_core_web_sm')
   ```

2. **Define the Text to Lemmatize** 📝
   ```python
   text = "The quick brown foxes are jumping over the lazy dogs."
   doc = nlp(text)
   ```

3. **Extract Lemmatized Tokens** 🦊
   The code below processes the text and extracts the lemma of each word:
   ```python
   tokens = [token.lemma_ for token in doc]
   print(tokens)
   ```

4. **Observe the Output**
   Expected output:
   ```python
   ['the', 'quick', 'brown', 'fox', 'be', 'jump', 'over', 'the', 'lazy', 'dog', '.']
   ```

   As you can see, "foxes" becomes "fox" and "are jumping" is transformed to "be jump" due to the lemma extraction.

---

## 🧪 Task Objectives
- Experiment with different sentences and explore how lemmatization varies with context.
- Try implementing **NLTK’s WordNet Lemmatizer** as an additional exercise. This is included in the notebook, providing a comparison between the two methods.

---

## 🎯 Goal
By the end of this task, you should:
- Understand the basics of lemmatization in NLP.
- Know how to use spaCy and NLTK for lemmatization.
- Be able to transform text into its base forms, improving text analysis for future tasks.

---

## 💡 Tips
- Don’t forget to experiment with the part-of-speech (POS) tagging in spaCy! Lemmatization works best when the POS is correctly assigned.
- Keep an eye on words like "is", "are", "was" – their lemmatization might change depending on context.

---

## 📚 Resources
- [spaCy Documentation](https://spacy.io/usage)
- [NLTK Documentation](https://www.nltk.org/)

---

Happy coding! 💻✨

---