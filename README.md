# 🧠 Sentiment Analysis for Mental Health Statements

## 📌 Project Purpose

The purpose of this project was to explore and analyze emotional patterns in mental health-related statements using Natural Language Processing (NLP), SQL, and Power BI.  
By examining real-world mental health data, I aimed to detect tone and sentiment across categories like depression, anxiety, stress, and suicidal ideation.  
This project helped me apply machine learning techniques to text data, practice SQL-based analytics, and build a Power BI dashboard to present the insights in a visual, interactive way.

---

## 📁 Dataset Source

📦 [Sentiment Analysis for Mental Health – Kaggle Dataset](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health/data)  
The dataset combines cleaned and labeled statements from various mental health sources including:
- Reddit Mental Health Posts
- Suicidal Tweet Detection
- Depression and Bipolar Datasets
- Chatbot Conversations
- Anxiety, Stress, and Personality Disorders

Each entry includes:
- `statement`: The actual user message or post  
- `status`: The mental health condition label (e.g., Depression, Normal, Suicidal)

---

## 🔄 Project Workflow

### 🔹 Step 1: Data Cleaning (Excel + Python)

I began by removing empty rows and unnecessary columns in Excel. I trimmed whitespace, standardized capitalization, and ensured every record had both a statement and a status.

Then, I used Python to repeat the cleaning process programmatically, ensuring no nulls or invalid values remained. The text was preprocessed to prepare for sentiment analysis.

---

### 🔹 Step 2: Sentiment Analysis with TextBlob

After cleaning, I used the TextBlob library in Python to analyze the emotional tone of each statement. TextBlob calculates a sentiment polarity score for each entry, which I used to classify the sentiment into three categories:
- Positive
- Negative
- Neutral

These sentiment results were added to the dataset in two new columns: one for the numerical score and one for the label.

---

### 🔹 Step 3: SQL Integration and Analysis

I exported the dataset to CSV and loaded it into a MySQL database. I created a table for the data and used SQL to perform queries such as:
- Counting how many statements fall into each mental health status
- Analyzing sentiment label distribution
- Calculating the average sentiment score by mental health condition

These queries helped me better understand emotional trends across each mental health category.

---

### 🔹 Step 4: Visualization in Power BI

Using MySQL as a data source, I built an interactive dashboard in Power BI. The visualizations included:

- 📊 **Pie Chart**: Shows distribution of sentiment labels (positive, neutral, negative)
- 📈 **Clustered Column Chart**: Compares number of statements across different mental health statuses
- 📋 **Table**: Displays full statements with their sentiment and status
- 🎛️ **Slicer**: Lets the user filter all visuals by specific mental health status

---

## 📊 Data Summary

- Total Statements: **52,681**
- Status Breakdown:
  - Normal: 16,343
  - Depression: 15,404
  - Suicidal: 10,652
  - Anxiety: 3,841
  - Bipolar: 2,777
  - Stress: 2,587
  - Personality Disorder: 1,077

---

## ✅ Tools Used

- **Python** (pandas, textblob, Google Colab) – for cleaning and sentiment analysis
- **MySQL** – for structured storage and SQL queries
- **Excel** – for initial review and manual cleaning
- **Power BI** – for dashboard and visual insights

---

## 🧠 Conclusion

This project allowed me to analyze real-world mental health statements and identify sentiment trends across different mental health conditions.  
I built a complete workflow from raw data cleaning to final dashboard presentation using professional tools like Python, MySQL, and Power BI.  
This experience helped me improve my skills in data preprocessing, NLP, SQL analysis, and business intelligence reporting — all while working on a socially impactful problem.

---

## 📎 Files in This Repository

| File Name                       | Description                                  |
|--------------------------------|----------------------------------------------|
| `Combined Data.csv`            | Original raw dataset from Kaggle             |
| `Cleaned_Mental_Health.csv`    | Cleaned version used for analysis            |
| `mental_health_sentiment.csv`  | Final data with sentiment scores             |
| `Mental_Health_Sentiment.ipynb`| Colab notebook with Python processing        |
| `mental_health_sentiment.pbix` | Power BI dashboard file                      |
