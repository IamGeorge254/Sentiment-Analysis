# 📝 Consumer Complaint Sentiment Analysis & Dashboard

## 📌 Project Overview
This project focuses on analyzing U.S. consumer complaint narratives to understand customer sentiment.  
Using **Python (Pandas, NLTK – VADER)**, I classified complaint text into **Positive, Negative, or Neutral** sentiments.  
The results were then visualized in an **interactive Tableau dashboard** to highlight sentiment distribution, trends, and complaint categories.

Dataset Source: [Consumer Complaint Database (CFPB)](https://www.consumerfinance.gov/data-research/consumer-complaints/search/?chartType=line&company=EQUIFAX%2C%20INC.&dateInterval=Month&dateRange=1y&date_received_max=2025-09-11&date_received_min=2024-09-11&lens=Product&product=Credit%20card&searchField=all&subLens=sub_product&tab=Trends)

---

## ⚙️ Tools & Technologies
- **Python**: Pandas, NLTK (VADER Sentiment Analyzer), tqdm  
- **Tableau**: For dashboard and data storytelling  
- **Jupyter Notebook**: Data exploration and preprocessing  

---

## 🚀 Steps I Took

### 1. Data Collection
- Downloaded consumer complaint data from CFPB’s official portal.  
- Focused on **credit card complaints** for EQUIFAX, INC. (last 12 months).  

### 2. Data Cleaning & Preprocessing
- Checked for missing values in **Consumer complaint narrative**.  
- Created a helper column `text_status`:
  - `"No text"` if the narrative was missing.  
  - `"To analyze"` if text was available.  
- Standardized text for sentiment analysis.

### 3. Sentiment Analysis
- Implemented **NLTK’s VADER** model.  
- Generated two new features:
  - `sentiment_score` → VADER compound score.  
  - `sentiment_label` → categorized as *Positive, Negative, Neutral, or No text*.  
- Used **tqdm** for progress tracking while applying sentiment analysis across rows.

### 4. Dashboard Development
- Exported processed data into Tableau.  
- Built an **interactive dashboard** to display:
  - Sentiment distribution (Positive/Negative/Neutral).  
  - Complaint trends over time.  
  - Comparison of products and sub-products by sentiment.  

---

## 📊 Tableau Dashboard
View the live dashboard here:
[Complaints Dashboard](https://public.tableau.com/app/profile/george.mwaura/viz/ComplaintsDashboard_17579396550350/Dashboard1)

---

## 📈 Key Insights
- Most complaints tend to have **Positive sentiment**, reflecting frustration in consumer narratives.
- Negative sentiment (46%) is nearly as common, highlighting widespread dissatisfaction and unresolved issues.
- A small proportion of complaints fall under Neutral sentiment, indicating balanced or factual reporting without strong emotions.
- At the product level (e.g., Debt Collection, Credit Card, Credit Card or Prepaid Card), there is an almost equal distribution between positive and negative complaints.
- Complaints by Month line chart shows that positive and negative sentiments follow very similar patterns across the year, while neutral complaints remain consistently low.

---
