# Hasaki Aspect Sentiment Analytics
---
## Introduction

This project focuses on crawling customer reviews from Hasaki.vn, a leading beauty e-commerce platform in Vietnam, and applying Aspect-Based Sentiment Analysis (ABSA) techniques. It includes:

- Web scraping feedback data using Selenium.  
- Automatic aspect and sentiment labeling using Gemini API.  
- Data preprocessing and NLP modeling to classify sentiment per aspect.  
- Visualization dashboards in Power BI for actionable insights.

---

## Objectives

This project aims to:

- Collect real customer feedback to analyze satisfaction and pain points.  
- Develop machine learning models to classify sentiment (positive, neutral, negative) by aspect (Quality, Packaging, Price, Service, Store, Miscellaneous).  
- Provide insights for business decision-making through data visualization dashboards.

---

## Dataset

**Source:** Crawled from [Hasaki.vn](https://hasaki.vn/) using Selenium.

**Content:** Product reviews including:

- Product name, category, price, rating, number of purchases.  
- Customer name, comment content, rating score, timestamp.

---

## Data Labeling Approach

Used Gemini API to automatically label aspect and sentiment for each sentence. After auto-labeling, we performed manual validation to check and correct mislabeling cases, ensuring high-quality labeled data for model training.

### Sentiment labels (3):

- Positive  
- Negative  
- Neutral

### Aspect labels (6):

- PACKAGING  
- QUALITY  
- PRICE  
- SERVICE  
- STORE  
- MISCELLANEOUS

---

## Project Structure

```
Hasaki_NLP_Analytics/
├── code_crawl_data/        # Web scraping (Selenium) and NLP preprocessing
├── code_model/             # Model training 
├── data/                   # Raw and processed datasets
├── model/                  # Saved ML models
├── Hasaki_Analytics.pbix   # Power BI dashboard file
├── Hasaki_Analytics.pdf    # Dashboard report export
├── BAOCAOWORD.pdf          # Full project report (Vietnamese)
├── requirements.txt        # Python dependencies
├── runtime.txt             # Runtime environment
└── README.md               # Project overview
```

---

## Methods & Models

### Data Preprocessing

- Lowercasing, removing special characters, tokenization.  
- Stop words removal, lemmatization.  
- Word embedding using Word2Vec.

### Modeling

Compared multiple ML models:

- Logistic Regression  
- Support Vector Machine  
- Random Forest  
- Naïve Bayes  
- Neural Network

**Evaluation:** Accuracy, Precision, Recall, F1-Score, Confusion Matrix, ROC-AUC.
**Model selection:** Chose the best-performing model for each aspect-sentiment combination.

### Dashboard

Developed with Power BI to visualize:

- Sentiment distribution by aspect  
- Top positive/negative aspects  
- Product performance summaries
You can access the dashboard by opening the Hasaki_Analytics.pbix file using Power BI Desktop.
---

## Key Results & Insights

- Built a robust NLP pipeline to label and classify customer feedback automatically.  
- Identified main pain points and praised features across products.  
- Developed a dashboard for easy monitoring and strategic decision-making.

---

## Future Work

- Automate the data crawling and updating process by scheduling scripts and storing the data directly into a database, enabling seamless data integration and scalability. 
- Deploy as a Streamlit web app for live sentiment analysis.

---

## Learning Outcomes

Through this project, I have:

- Developed skills in web scraping with Selenium to extract large-scale product reviews.  
- Applied Gemini API for automated NLP labeling, enhancing annotation efficiency.  
- Strengthened knowledge in NLP preprocessing techniques, including tokenization and embeddings.  
- Gained practical experience in training and evaluating multiple ML models for text classification.  
- Built Power BI dashboards to communicate NLP results into actionable business insights.  
- Learned to manage a full ML pipeline from data collection to labeling, preprocessing, modeling, and visualization.

---

## Prerequisites

- Python 3.11  
- Selenium  
- Power BI Desktop  
- GitHub  
- Other Python libraries listed in `requirements.txt`

---

## Installation

### Clone the repository:

```bash
git clone https://github.com/yourusername/Hasaki_NLP_Analytics.git
cd Hasaki_NLP_Analytics
```

### Install dependencies:

```bash
pip install -r requirements.txt
```

### Run project:

1. Run data crawling scripts in `code_crawl_data/` to update the dataset.  
2. Execute NLP modeling scripts in `code_model/` to train or test models.  
3. Open `Hasaki_Analytics.pbix` with Power BI Desktop to explore the dashboard.

> **Note:** API key setup for Gemini API is required before running labeling scripts (not included in repo).

---
