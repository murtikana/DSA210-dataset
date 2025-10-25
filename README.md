# Steam Game Recommendation and Exploratory Data Analysis

**Author:** Muratcan Gülcan  
**Course:** DSA210 - Introduction to Data Science  
**Term:** 2025–2026 Fall  

---

## Project Overview

This project analyzes Steam user reviews to understand what factors influence whether a game is recommended or not.  
It combines **exploratory data analysis (EDA)** and a **machine learning model** to identify patterns in playtime, pricing, ratings, and platform availability.

---

## Motivation

Steam is the largest gaming platform with millions of user reviews.  
By analyzing these reviews, we can discover what drives players to recommend games — helping developers improve pricing, design, and platform strategies.

---

## Data Source

[Dataset Link](https://www.kaggle.com/datasets/antonkozyriev/game-recommendations-on-steam/data)

Files used:
- **games.csv:** Game metadata (ratings, prices, release years)
- **users.csv:** Public user info
- **recommendations.csv:** User reviews (recommended / not recommended)

---

## Methods

1. **Preprocessing**
   - Merged three datasets
   - Created new features: `age_at_review`, `platforms`, and `reviews_bin`
   - Cleaned missing or invalid values

2. **Exploratory Data Analysis**
   - Visualized distributions of playtime, price, and ratings  
   - Examined correlations and trends over time  
   - Found patterns by platform and rating category  

3. **Machine Learning**
   - Random Forest Classifier predicting `is_recommended`
   - Features: playtime, price, positive ratio, user reviews, release age, platforms  
   - Accuracy: **~85%**, precision and recall above 0.88

---

## Key Findings

- Most reviews (≈87%) are positive.  
- “Very Positive” and “Positive” games dominate Steam’s catalog.  
- Multi-platform games reach up to **94%** recommendation rates.  
- Higher playtime strongly correlates with positive reviews.  
- Recommendation rates slightly declined from 2011–2021, peaking during Steam sales.

---

## Limitations & Future Work

- Dataset was pre-cleaned, limiting access to raw data patterns.  
- Only numeric features were used — no review text analysis yet.  
- Future work: add **sentiment analysis**, **genre-based modeling**, and **price inflation adjustments**.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/steam-recommendation.git
   cd steam-recommendation

pip install -r requirements.txt
jupyter notebook gamerecommendation.ipynb

Requirements
pandas
numpy
matplotlib
seaborn
scikit-learn

AI Assistance Disclosure

Some text formatting and documentation improvements were supported by ChatGPT (GPT-5).
All code, analysis, and interpretations were independently written and verified by Muratcan Gülcan.

Citation

Kozyriev, Anton. Game Recommendations on Steam. Kaggle, 2022.
Sabancı University, DSA210 – Introduction to Data Science, Fall 2025–2026 Project Guidelines.



