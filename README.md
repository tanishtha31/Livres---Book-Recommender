# Livres
**A book recommendation engine that helps readers discover their next favourite book.**
## Table of Contents
- [Overview](#overview)
- [Project Files Explanation](#project-files-explanation)
- [How To Use The Engine](#how-to-use-the-engine)
- [Dataset](#dataset)
- [Packages](#packages)
---
## Overview
Build an Intelligent book recommendation system using the power of large language models and Python. Transformed book descriptions into mathematical representations that enable precise content based matching.
Used Zero-Shot Classification to classify book descriptions and checked classifier accuracy, also applied fine tuned LLMs for Sentiment analysis.
Key Concepts : Sematics, Zero-shot learning, Natural language processing, Machine learning, Deep learning, Data Science, API, Transformer, Vector, Word embedding.
---
## Project Files Explanation
**Data - explanation**
- Read the data with the help of Pandas (pd.read_csv)
- Found missing observations
- Checked if missing observations have a pattern
- Deleted 303 rows of observation because they missed descriptions.
- Checked how many words in a sentence would make a description meaningful as there were descriptions in the data with very less meaning.
- Aggregated title and subtitle together.
- Joined isbn numbers to the beginning of the book description sentences to use them in the vector classification and named the text file **books_cleaned.csv**
---
**Vector Search**
- Imported books_cleaned.csv
- As user should get the book title and author but vector would give the description, we split the isbn number which we earlier attached to the description when we get recommendations.
- Later ran a query to test whether the method of giveing out recommendation according to the user input is working correctly using similarity search.
---
**Text Classifier**
- Figuring out Categories of the books i.e.Fiction,NonFiction etc.
- Sorting the pieces of text into certain categories through Zero-short Classification.
- Saving the file with the name books_with_categories.csv
---
**Sentiment Analysis**
- Worked on finding out the emotion (Sadness or Happy) of the text description with the help of Sentiment Classifier Model from Huggingface by breaking the paragraph into sentences and checking the emotion for each sentence to get a major emotion.
- saving the file with the name books_with_emotions.csv
---
**Gradio**
- Read books_with_emotions.csv
- Named the dashboard Livres and added Selection columns through which users would interact. 
---
## Screenshots of the Demo
<img width="1243" height="983" alt="Book Recommender" src="https://github.com/user-attachments/assets/64a97e67-8775-409d-a429-3725a73b9bad" />

---
<img width="1247" height="965" alt="book recommender 2" src="https://github.com/user-attachments/assets/337fd9f0-3575-48fd-a271-b10cc02ba024" />

---

## How to use the engine
In the above images there are three Select boxes namely, **Please enter a description of a book**, **Select a category**, **Seclect an emotion** where the user has to describe a book in English words, select between categories like Fiction, Nonfiction etc, and Choose an emotion like Sadness, happy, etc, respectively and click on Find Recommendations.

---
## Datasets
**Source** : Kaggle.com/datasets

**Dataset name** : 7k Books

---

## Packages
- Kagglehub
- Pandas
- Matplotlib
- Seaborn
- Python-dotenv
- Langchain-community
- langchain-Chroma
- Embedding Model - all-MiniLM-L6-v2 (Free sentence embeddings from Hugging Face)
- Transformers
- Gradio
- Notebook
- ipy Widgets
---

