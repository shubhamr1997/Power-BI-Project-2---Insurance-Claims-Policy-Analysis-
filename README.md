# 🛡️ Insurance Analytics & Customer Sentiment — Power BI

## 📌 Project Overview

This Power BI project analyzes insurance policy, premium, claim, coverage, and customer feedback data.

The project combines:

**Power BI Dashboarding → Interactive Filtering → Drill-Through Analysis → Python Sentiment Analysis → Customer Feedback Insights**

The main insurance dashboard was built using a single **InsuranceData** table, while customer sentiment analysis was performed using a separate **Feedback** table.

---

## 🎯 Project Objectives

- Analyze insurance premium, claim, and coverage amounts.
- Understand policy distribution across different policy types.
- Analyze active and inactive policies.
- Examine claim status distribution.
- Analyze claim amounts across age groups.
- Explore policy and claim details through a detailed table and drill-through filtering.
- Analyze customer feedback using sentiment analysis.
- Categorize customer feedback based on sentiment score.

---

# 📊 Power BI Dashboard

## 1. 🏠 Insurance Dashboard

The main dashboard uses the **InsuranceData** table and provides an overview of insurance performance and policy activity.

### Key Analysis

- **Premium Amount**
- **Claim Amount**
- **Coverage Amount**
- Premium Amount by Policy Type
- Active vs Inactive Policies
- Claim Status Distribution
- Claim Amount by Age Group
- Gender Distribution
- Policy Type and Claim Status analysis

![Insurance Dashboard](images/dashboard.png)

---

## 2. 🔎 Table Visual & Drill-Through

A detailed table was created using the **InsuranceData** table to allow users to explore policy-level and claim-level records.

The table includes information such as:

- Policy Number
- Customer ID
- Claim Number
- Age
- Gender
- Coverage Amount
- Premium Amount
- Policy Start Date
- Policy End Date
- Policy Type
- Claim Status
- Claim Date
- Claim Amount

A drill-through filter was also implemented to allow more detailed exploration based on selected policy attributes.

![Table Visual & Drill Through](images/drill-through.png)

---

# 🧠 Customer Sentiment Analysis

## 3. 💬 Sentiment Analysis

Customer feedback was analyzed separately using the **Feedback** table.

The feedback data contains:

- Customer Name
- Feedback
- Sentiment Score
- Good / Improvement category

The sentiment score was generated using **Python and Jupyter Notebook** before the data was used in Power BI.

### Python Sentiment Analysis

The Jupyter Notebook uses:

- **Python**
- **Pandas**
- **NLTK**
- **VADER SentimentIntensityAnalyzer**

The VADER compound sentiment score was normalized to a **0–1 scale** using:

```python
(sia.polarity_scores(text)['compound'] + 1) / 2
```

The resulting `sentiment_score` was added to the feedback dataset and the processed data was exported back to Excel for use in Power BI.

### Sentiment Categorization

A conditional column was created in Power BI to classify customer feedback into:

- **Excellent**
- **Good**
- **Needs Improvement**

These categories were based on the calculated sentiment score.

![Sentiment Analysis](images/sentiment-analysis.png)

---

## 📈 Sentiment Dashboard

The sentiment analysis page combines:

- Customer feedback text
- Sentiment score
- Customer-level feedback table
- Feedback category counts
- Word cloud visualization

This allows customer feedback to be analyzed both quantitatively through sentiment scores and qualitatively through the written feedback.

---

# 🔄 Project Workflow

```text
Insurance Data
      │
      ▼
   Power BI
      │
      ├── Dashboard
      ├── Interactive Filters
      └── Drill-Through Analysis


Customer Feedback
      │
      ▼
Python / Jupyter Notebook
      │
      ├── Pandas
      ├── NLTK
      └── VADER Sentiment Analysis
              │
              ▼
      Sentiment Score (0–1)
              │
              ▼
           Power BI
              │
              ▼
      Sentiment Analysis
```

---

# 🛠️ Skills Demonstrated

### 📊 Power BI

- Dashboard development
- Interactive filters and slicers
- Drill-through analysis
- Table visual analysis
- Data visualization
- Business-focused reporting

### 🧹 Data Preparation

- Working with structured insurance data
- Working with customer feedback data
- Conditional column creation
- Preparing sentiment results for reporting

### 🐍 Python

- Python data processing
- Pandas
- NLTK
- VADER sentiment analysis
- Sentiment score normalization

### 💬 Customer Analytics

- Customer feedback analysis
- Sentiment scoring
- Sentiment categorization
- Text-based customer insight analysis

---

## ⚙️ Tools & Technologies

`Power BI` • `Python` • `Jupyter Notebook` • `Pandas` • `NLTK` • `VADER`

---

## 📁 Project Structure

```text
Insurance-Analytics-PowerBI/
│
├── README.md
├── Insurance-Analytics.pbix
├── sentimentanalysis.ipynb
└── images/
    ├── dashboard.png
    ├── drill-through.png
    └── sentiment-analysis.png
```

---

# ✅ Conclusion

This project demonstrates how Power BI can be combined with Python-based sentiment analysis to create a broader insurance analytics solution.

The project covers:

**Insurance Data Analysis → Interactive Reporting → Drill-Through → Customer Feedback Processing → Sentiment Analysis → Business Insights**
