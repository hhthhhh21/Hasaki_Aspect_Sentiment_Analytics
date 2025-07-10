# Hasaki_Aspect_Sentiment_Analytics
Project Title
Hasaki NLP Analytics

Introduction
This project focuses on crawling customer reviews from Hasaki.vn, a leading beauty e-commerce platform in Vietnam, and applying Aspect-Based Sentiment Analysis (ABSA) techniques. It includes:

Web scraping feedback data using Selenium.

Automatic aspect and sentiment labeling using Gemini API.

Data preprocessing and NLP modeling to classify sentiment per aspect.

Visualization dashboards in Power BI for actionable insights.

Project Motivation & Objectives
With the boom in e-commerce, understanding customer sentiment becomes crucial for business success. This project aims to:

Collect real customer feedback to analyze satisfaction and pain points.

Develop machine learning models to classify sentiment (positive, neutral, negative) by aspect (Quality, Packaging, Price, Service, Store, Miscellaneous).

Provide insights for business decision-making through data visualization dashboards.

Dataset
Source: Crawled from Hasaki.vn using Selenium.

Content: Product reviews including:

Product name, category, price, rating, number of purchases.

Customer name, comment content, rating score, timestamp.

Data Labeling Approach
Used Gemini API to automatically label:

Sentiment labels (3):

Positive

Negative

Neutral

Aspect labels (6):

PACKAGING

QUALITY

PRICE

SERVICE

STORE

MISCELLANEOUS

Each comment was split into sentences, and each sentence received exactly one aspect label and one sentiment label.

Project Structure
bash
Copy
Edit
Hasaki_NLP_Analytics/
├── code_crawl_data/        # Web scraping scripts (Selenium)
├── code_model/             # NLP preprocessing and model training scripts
├── data/                   # Raw and processed datasets (CSV)
├── model/                  # Saved ML models
├── Hasaki_Analytics.pbix   # Power BI dashboard file
├── Hasaki_Analytics.pdf    # Dashboard report export
├── BAOCAOWORD.pdf          # Full project report (Vietnamese)
├── requirements.txt        # Python dependencies
├── runtime.txt             # Runtime environment
└── README.md               # Project overview
Methods & Models
Data Preprocessing
Lowercasing, removing special characters, tokenization.

Stop words removal, lemmatization.

Word embedding using Word2Vec.

Modeling
Compared multiple ML models:

Logistic Regression

Support Vector Machine

Random Forest

Naïve Bayes

Artificial Neural Network (ANN)

Evaluation: Accuracy, Precision, Recall, F1-Score, Confusion Matrix, ROC-AUC.

Model selection: Chose the best-performing model for each aspect-sentiment combination.

Dashboard
Developed with Power BI to visualize:

Sentiment distribution by aspect

Top positive/negative aspects

Product performance summaries

Key Results & Insights
Built a robust NLP pipeline to label and classify customer feedback automatically.

Identified main pain points and praised features across products.

Developed a dashboard for easy monitoring and strategic decision-making.

Future Work
Enhance NLP preprocessing to handle Vietnamese slang, abbreviations, and spelling errors.

Improve labeling accuracy by combining Gemini API with manual validation.

Expand dataset to include more product categories.

Deploy as a Streamlit web app for live sentiment analysis.

Learning Outcomes
Through this project, I have:

Developed skills in web scraping with Selenium to extract large-scale product reviews.

Applied Gemini API for automated NLP labeling, enhancing annotation efficiency.

Strengthened knowledge in NLP preprocessing techniques, including tokenization and embeddings.

Gained practical experience in training and evaluating multiple ML models for text classification.

Built Power BI dashboards to communicate NLP results into actionable business insights.

Learned to manage a full ML pipeline from data collection to labeling, preprocessing, modeling, and visualization.

Prerequisites
Python 3.11

Selenium

Streamlit (optional for web app deployment)

Power BI Desktop

GitHub

Other Python libraries listed in requirements.txt

Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/Hasaki_NLP_Analytics.git
cd Hasaki_NLP_Analytics
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run data crawling scripts in code_crawl_data/ to update the dataset.

Execute NLP modeling scripts in code_model/ to train or test models.

Open Hasaki_Analytics.pbix with Power BI Desktop to explore the dashboard.
