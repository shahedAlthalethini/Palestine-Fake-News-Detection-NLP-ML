Palestine Fake News Detection using NLP & ML 🇵🇸
📌 Overview
A machine learning project designed to detect fake news in Palestinian media using Natural Language Processing (NLP) and classification models. The system includes a full pipeline from data collection to web deployment using FastAPI and React.

🧠 Features
Custom Dataset from Telegram groups and Palestinian news channels.
Preprocessing Pipeline for Arabic text cleaning and normalization.
ML Models: Trained multiple classifiers (e.g. Logistic Regression, Naive Bayes).
Web Interface: Built with React.js.
API Backend: Powered by FastAPI.
Visualization: Interactive display of model performance and predictions.

🧪 Dataset
Collected manually from Telegram channels and news groups during multiple months.
Combined all CSVs into a single file: monthly_raw_data/merged_cleaned.csv.
Labeled as Fake or Real manually.
Contains Arabic text entries.

🗂️ Dataset Description
Sources: Multiple Arabic news platforms.
Language: Modern Standard Arabic (MSA).
Classes: Real (~73%), Fake (~27%).
Attributes: Title, content, date, source platform, label.

📊 Exploratory Data Analysis
Imbalance: Notable skew toward real news.
Temporal patterns: Most content from 2024.
Source diversity: Includes trusted and less reliable platforms.
Challenges: Class imbalance, inconsistent article quality.

⚙️ Preprocessing Pipeline
Text Cleaning:
Remove URLs, HTML, emojis, diacritics.
Normalize Arabic letters (e.g. آ, أ → ا).
Stop Word Removal:
Used both NLTK and custom Arabic stop words lists.
Named Entity Recognition (NER):
Used Stanza to extract/remove entities.
Lemmatization:
Standardized words using morphological analysis (Stanza).
Vectorization:
TF-IDF with unigrams and bigrams (top 5000 features).
