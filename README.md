# 📰 Fake News Detection in Arabic News Articles  


---

## 📌 Project Overview

This project focuses on detecting fake news in Arabic news articles using Natural Language Processing (NLP) and machine learning techniques. We explored both classical and deep learning models to classify news content as either *real* or *fake*.

---

## 🧠 Objectives

- Build a complete Arabic NLP preprocessing pipeline.
- Evaluate classical ML models and BERT for fake news classification.
- Analyze linguistic differences between fake and real news.
- Contribute to the field of Arabic NLP and misinformation detection.

---

## 🗂️ Dataset Description

- **Sources:** Multiple Arabic news platforms.
- **Language:** Modern Standard Arabic (MSA).
- **Classes:** Real (~73%), Fake (~27%).
- **Attributes:** Title, content, date, source platform, label.

---

## 📊 Exploratory Data Analysis

- **Imbalance:** Notable skew toward real news.
- **Temporal patterns:** Most content from 2024.
- **Source diversity:** Includes trusted and less reliable platforms.
- **Challenges:** Class imbalance, inconsistent article quality.

---

## ⚙️ Preprocessing Pipeline

1. **Text Cleaning:**
   - Remove URLs, HTML, emojis, diacritics.
   - Normalize Arabic letters (e.g. آ, أ → ا).

2. **Stop Word Removal:**
   - Used both NLTK and custom Arabic stop words lists.

3. **Named Entity Recognition (NER):**
   - Used Stanza to extract/remove entities.

4. **Lemmatization:**
   - Standardized words using morphological analysis (Stanza).

5. **Vectorization:**
   - TF-IDF with unigrams and bigrams (top 5000 features).

---

## 🧪 Models & Techniques

| Model               | Type               | Notes |
|--------------------|--------------------|-------|
| **Logistic Regression** | Classical ML       | Fast and interpretable baseline |
| **Support Vector Machine (SVM)** | Classical ML       | High-dimensional performance |
| **Random Forest**   | Ensemble ML        | Non-linear modeling, robust |
| **XGBoost**         | Ensemble ML        | High accuracy, handles imbalance |
| **Arabic BERT**     | Deep Learning (Transformer) | Used pre-trained `asafaya/bert-mini-arabic` |

---

## 📈 Performance Metrics

| Model             | Accuracy | F1-Score | Precision | Recall | Training Time |
|------------------|----------|----------|-----------|--------|----------------|
| **BERT**          | 85.2%    | 0.83     | 0.85      | 0.84   | High            |
| **Logistic Reg.** | 89.3%    | 0.87     | 0.89      | 0.89   | Low             |
| **SVM**           | 90.1%    | 0.88     | 0.90      | 0.90   | Medium          |
| **Random Forest** | 99.9%    | 0.88     | 0.85      | 0.84   | Medium          |
| **XGBoost**       | 98.8%    | 0.89     | 0.87      | 0.84   | Medium          |

> ⚠️ Note: Random Forest's high accuracy with lower F1 suggests possible overfitting due to class imbalance.

---

## 📉 Evaluation Highlights

- **AUC-ROC:** High values indicate good class separability.
- **N-gram Insights:** Real news uses formal, named entities; fake news has sensational and emotional language.
- **Classical Models vs BERT:** With limited data, classical models outperformed BERT in accuracy and efficiency.

---

## 🧩 Challenges

- Imbalanced dataset.
- Arabic morphology and syntax complexity.
- Limited resources for Arabic NLP tools and annotated data.

---

## 🚀 Future Work

### Short-term
- Expand fake news samples.
- Perform hyperparameter optimization.
- Conduct error analysis.

### Long-term
- Add dialect support.
- Integrate multimedia and metadata (images, videos).
- Real-time detection tools.
- Cross-lingual detection using multilingual models.

---

## 🌐 Real-World Applications

- News platform integration.
- Government misinformation detection tools.
- Social media fake content filtering.

---

## 🛠️ Technologies Used

- Python, Scikit-learn, XGBoost, NLTK, Stanza, Hugging Face Transformers  
- Jupyter Notebook, Google Colab  

---

## 🙏 Acknowledgments

Special thanks to **Dr. Tareq AlTalmas** for his guidance and support throughout this project.s).
