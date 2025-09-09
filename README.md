# Yelp User & Business Recommendation Analysis

## 1. Project Overview
This project explores the **Yelp dataset** to build user profiles, analyze business features, and generate personalized user–business recommendations.  
It combines **data preprocessing, feature engineering, user profiling, topic modeling, and machine learning** to provide both descriptive insights and predictive recommendations.

---

## 2. Data Processing
- Cleaned and preprocessed raw Yelp data for consistency and efficiency.
- Selected essential variables: friends, elite years, votes, compliments, and attributes.
- Converted `yelping_since` to datetime and merged **business**, **user**, and **review** tables.
- Filtered data between **2020–2022** and applied a **10% stratified sample**.
- Missing values handled systematically:
  - Numbers → filled with 0  
  - Categories → `"Unknown"`  
  - Attributes → empty dictionaries  

👉 Built a clean, standardized foundation for reliable analysis.

---

## 3. Data Analysis

### 1. General Characteristics
- Most numeric variables (review counts, fans) follow **long-tail distributions**.
- Restaurants dominate Yelp’s categories, especially food-related businesses.
- Common attributes: **credit card acceptance** and **parking**.  

👉 Provided macro-level understanding of the dataset.


### 2. User Profiling
- **Lifecycle Stage**: new, intermediate, and long-term users (based on registration vs. first review).  
- **Activity Level**: clustered into *high*, *moderate*, and *low activity*.  
- **Review Quality & Recognition**: grouped into *opinion leaders* vs. *low-engagement* users.  
- **Social Influence**: identified high- vs. low-influence users using friends, fans, and interactions.  
- **Interest Topics**: LDA on categories revealed 10 themes (e.g., *Nightlife & Dining*, *Beauty & Health*).  

👉 Built a comprehensive **user persona system** for targeted engagement.


### 3. Business Feature Analysis
- Flattened and analyzed attributes by both **frequency** and **impact on ratings/reviews**.
- Findings: **rare attributes** (e.g., Wi-Fi, outdoor seating) drive more positive ratings than basic features.  

👉 Showed that **differentiation** is key for customer satisfaction.


### 4. User–Business Recommendation
- Combined **user tags** with **business features**.
- Defined user preferences: reviews ≥ 4 stars = *like*.  
- Trained a **Random Forest classifier** to predict matches.
- Generated **Top-5 personalized recommendations per user**.  

👉 Achieved **personalized and precise recommendations**.

---

## 4. Tech Stack
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)  
- **NLP / Topic Modeling**: LDA (Scikit-learn / Gensim)  
- **Machine Learning**: K-Means, Random Forest Classifier  
- **Visualization**: Matplotlib  

---

## 5. Results
- Clear **user personas** based on lifecycle, activity, quality, and influence.
- Identified **key business attributes** linked to higher ratings.
- Built a **hybrid recommendation system** leveraging both user and business features.
- Improved personalization and conversion potential.

---

## 6. Acknowledgements
Dataset provided by [Yelp Open Dataset](https://business.yelp.com/data/resources/open-dataset/).
