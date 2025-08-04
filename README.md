# BBC_Archivied-NLP-Project

This project is part of my personal challenge to build one small but meaningful NLP or ML project every day.

In this project, I trained a text classification model to categorize archived BBC news articles into one of the following categories:

- **Business**
- **Entertainment**
- **Politics**
- **Sport**
- **Tech**

---

## 📌 What the Project Does

Given the text of a news article, the model predicts its category using natural language processing techniques. It’s a multi-class classification problem trained on real BBC news data.

---

## 📂 Dataset

- The dataset contains news articles along with their categories.
- Columns include: `title`, `content`, and `category`.
- Total records: ~2,200
- File: `bbc-news-data.csv`
- Source: BBC Archive (cleaned and tab-separated)

---

## 🔍 How It Works

1. **Data Preprocessing**
   - Combined `title` and `content` for better context
   - Removed the `filename` column
   - Handled tab-separated format and missing values

2. **Text Vectorization**
   - Used **TF-IDF Vectorizer** with English stopword removal

3. **Model Training**
   - Model: **Logistic Regression**
   - Split: 80% training, 20% testing
   - Accuracy: ~95% on test data

4. **Evaluation**
   - Accuracy Score
   - Classification Report (Precision, Recall, F1)
   - Confusion Matrix (visualized with Seaborn)

5. **Testing with Custom Sentences**
   - The model can predict the category for any given sentence like:
     - “The government passed a new healthcare bill.” → *Politics*
     - “Apple unveils new AI-powered MacBooks.” → *Tech*

## 📈 Sample Results

