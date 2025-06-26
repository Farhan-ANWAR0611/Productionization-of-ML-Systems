# Productionization-of-ML-Systems
# 🏨 Hybrid Hotel Recommendation System

This project is a part of a **Travel Capstone Project** which implements a **Hotel Recommendation System** using a hybrid approach combining **Collaborative Filtering** and **Content-Based Filtering**. The final model is deployed as a **Streamlit web application**, allowing users to enter their user ID and receive top hotel recommendations.

---

## 📁 Dataset Overview

The dataset contains real user hotel bookings with the following features:

- `travelCode`: Unique travel transaction ID  
- `userCode`: Unique identifier for the user  
- `name`: Hotel name  
- `place`: Hotel location  
- `days`: Duration of stay  
- `price`: Cost per day  
- `total`: Total cost paid  
- `date`: Booking date

---

## ✅ Key Features

### 1. Data Cleaning & Preprocessing
- Removed missing or duplicated entries  
- Converted date strings to proper datetime format  
- Normalized textual and numerical values  
- Counted number of unique users and hotels

### 2. Collaborative Filtering (CF)
- Used `Surprise` library's `KNNBasic` algorithm  
- Treated the `total` cost as an implicit rating  
- Evaluated with RMSE (Root Mean Squared Error)  
- Final model achieved **RMSE ≈ 0.97**

### 3. Content-Based Filtering (CBF)
- Vectorized hotel names and places using TF-IDF  
- Computed hotel similarity using cosine similarity  
- Identified similar hotels based on user history

### 4. Hybrid Recommender System
- Combined CF and CBF with a weighted score  
- Final score = 70% CF prediction + 30% CBF similarity  
- Produced better personalized hotel recommendations

### 5. Streamlit Web Application
- Simple UI: Input user ID and get top hotel suggestions  
- Built using `streamlit` and deployed via `ngrok`  
- Real-time hotel recommendation system

---

## 🚀 How to Run Locally

### Step 1: Install dependencies
```bash
pip install pandas numpy scikit-learn streamlit pyngrok scikit-surprise
