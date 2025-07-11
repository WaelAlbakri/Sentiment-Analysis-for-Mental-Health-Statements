# 🧠 Sentiment Analysis for Mental Health Statements

## 📌 Project Purpose

The purpose of this project was to explore and analyze emotional patterns in mental health-related statements using Natural Language Processing (NLP), SQL, and Power BI.  
By examining real-world mental health data, I aimed to detect tone and sentiment across categories like depression, anxiety, stress, and suicidal ideation.  
This project helped me apply machine learning techniques to text data, practice SQL-based analytics, and build a Power BI dashboard to present the insights in a visual, interactive way.

---

## 🗂️ About the Dataset

Below is the original dataset description written by the Kaggle publisher **Suchintika Sarkar**:

> This comprehensive dataset is a meticulously curated collection of mental health statuses tagged from various statements. The dataset amalgamates raw data from multiple sources, cleaned and compiled to create a robust resource for developing chatbots and performing sentiment analysis.

### 📚 Data Sources

The dataset integrates information from the following Kaggle datasets:

- 3K Conversations Dataset for Chatbot  
- Depression Reddit Cleaned  
- Human Stress Prediction  
- Predicting Anxiety in Mental Health Data  
- Mental Health Dataset Bipolar  
- Reddit Mental Health Data  
- Students Anxiety and Depression Dataset  
- Suicidal Mental Health Dataset  
- Suicidal Tweet Detection Dataset  

### 🧾 Data Overview

The dataset includes:

- `statement`: The textual data or post  
- `status`: The tagged mental health status  
  - Normal  
  - Depression  
  - Suicidal  
  - Anxiety  
  - Stress  
  - Bi-Polar  
  - Personality Disorder  

### 🌐 Data Collection

Data was collected from diverse platforms such as Reddit, Twitter, and other social media sources, making it valuable for:

- Developing intelligent mental health chatbots  
- Performing in-depth sentiment analysis  
- Academic research on mental health trends  

### 🔍 Features

- `unique_id`: Unique identifier for each entry  
- `statement`: The raw text data  
- `mental_health_status`: The annotated mental health category  

### 🙏 Acknowledgments

This dataset was created by aggregating and cleaning data from publicly available Kaggle datasets. Thanks to all original dataset creators for their contributions.

---

## 🔄 Project Workflow

### 🔹 Step 1: Data Cleaning (Excel + Python)
- Cleaned the dataset in Excel (removed blanks, trimmed spaces, unified casing)
- Repeated cleaning in Python with `pandas`: dropped nulls, applied `.strip()` and `.lower()`

### 🔹 Step 2: Sentiment Analysis (Python)
- Used `TextBlob` in Google Colab to assign a sentiment score between -1 and 1
- Classified each score into:
  - Positive: > 0.1
  - Neutral: between -0.1 and 0.1
  - Negative: < -0.1
- Stored results in new columns `sentiment_score` and `sentiment_label`

### 🔹 Step 3: SQL Analysis (MySQL)
- Exported processed data to CSV and imported into MySQL
- Created a table `mental_health` with sentiment metadata
- Ran SQL queries to analyze distribution and average scores per status

### 🔹 Step 4: Power BI Dashboard
- Connected Power BI to MySQL
- Created the following visuals:
  - 📊 Pie Chart – sentiment label distribution  
  - 📈 Clustered Column Chart – post count by mental health status  
  - 📋 Table – sample statements with sentiment data  
  - 🎛️ Slicer – to filter by mental health status  

---

## 📊 Summary Statistics

**Total statements:** 52,681  
**Status breakdown:**
- Anxiety: 3,841  
- Normal: 16,343  
- Depression: 15,404  
- Suicidal: 10,652  
- Stress: 2,587  
- Bipolar: 2,777  
- Personality Disorder: 1,077  

---

## 🛠️ Tools Used

- **Python** (pandas, textblob, Google Colab)  
- **MySQL** (data storage & queries)  
- **Power BI** (dashboard visualizations)  
- **Excel** (data cleanup)

---

## ✅ Outcome

This project allowed me to analyze real-world mental health statements and identify sentiment trends across various mental health statuses.  
I developed a full pipeline from raw data cleaning to final dashboard presentation using Excel, Python, SQL, and Power BI.  
This experience enhanced my skills in data wrangling, NLP, SQL querying, and data storytelling through visualization.

---

## 📎 Repository Files

| File Name                               | Description                                      |
|----------------------------------------|--------------------------------------------------|
| `Mental_Health_Sentiment.ipynb`        | Python notebook used in Google Colab            |
| `mental_health_sentiment.pbix`         | Power BI dashboard file                         |
| `Sentiment Analysis for Mental Health Statements.pdf` | Final report with full project explanation |
| `README.md`                            | This project overview                           |

---

## 🔗 Source

Original dataset on Kaggle by [Suchintika Sarkar](https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health)
