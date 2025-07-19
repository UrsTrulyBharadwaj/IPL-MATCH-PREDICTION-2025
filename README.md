# 🏏 IPL Match Prediction 2025  
![Python](https://img.shields.io/badge/Python-3.10-blue) 
![Machine Learning](https://img.shields.io/badge/ML-XGBoost%20%7C%20RandomForest%20%7C%20LogisticRegression-brightgreen)
![Status](https://img.shields.io/badge/Project-Complete-success)

## 📌 Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Dataset Overview](#dataset-overview)
- [Project Workflow](#project-workflow)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [Results & Evaluation](#results--evaluation)
- [Key Insights](#key-insights)
- [Limitations](#limitations)
- [Future Scope](#future-scope)
- [How to Run](#how-to-run)
- [Contact](#contact)

---

## 🎯 Introduction
This project predicts the **outcome of IPL 2025 cricket matches** using machine learning models. Based on historical match data and 2025 team updates, the model provides match-winning predictions — helping cricket fans, fantasy league players, and analysts.

---

## 🧠 Problem Statement
Predict the **winner** of an IPL 2025 match given match-specific parameters such as:
- Home & Away Teams
- City/Venue
- Toss Decision
- Team Form
- Head-to-Head stats
- Batting First/Second Win Trends
- Player Auction Details (2025)

---

## 📂 Dataset Overview
We used multiple datasets:
- `IPL_Historical_Data.csv` (2010–2024)
- `IPL_2025_Schedule.csv`
- `IPL_2025_Player_Auctions.csv`

Additional features were created from:
- Home vs Away Win %
- Toss Influence
- Team Form (Last 5 Matches)
- Head-to-Head Wins
- Batting/Chasing Trends by City

---

## 🔁 Project Workflow
1. ✅ Data Cleaning & Integration  
2. ✅ Feature Engineering  
3. ✅ Exploratory Data Analysis  
4. ✅ Model Selection & Training  
5. ✅ Hyperparameter Tuning  
6. ✅ Final Prediction Export

---

## ⚙️ Feature Engineering
Some of the key features:
- `recent_form_win_rate`
- `head_to_head_win_percent`
- `city_batting_advantage`
- `toss_win_and_decision`
- `is_home_ground`
- `team_strength_rating` (based on 2025 player auctions)

---

## 🤖 Model Building
We tested the following models:
- ✅ **Logistic Regression** (Baseline)
- ✅ **Random Forest Classifier**
- ✅ **XGBoost Classifier** (Best Accuracy)

**Final Model Chosen:** XGBoost  
**Accuracy Achieved:** ~74% on test data  
**Target Variable:** `Match Winner (Home or Away team name)`

---

## 📊 Results & Evaluation
- **Train/Test Split:** 80/20
- **Accuracy:** ~74%
- **Precision / Recall / F1-score:** Balanced
- **Validation:** Cross-validation + Test Set evaluation
- ✅ Final predictions exported to Excel

_Example Output:_

| Match No. | Home Team | Away Team | Winner Prediction |
|-----------|-----------|-----------|-------------------|
| 01        | CSK       | RCB       | CSK               |
| 02        | MI        | DC        | MI                |

---

## 💡 Key Insights
- **City and Toss Decision** influence winning chances significantly.
- Home ground advantage is real, but not in every city.
- Teams with better recent form tend to win more.
- Auction impact: New players shift team strength visibly.

---

## ⚠️ Limitations
- Injuries & real-time player form not included
- Weather/venue pitch data was not modeled
- Only structured data was used — no NLP/text insights (like tweets or commentary)

---

## 🔮 Future Scope
- Add **live match updates or ball-by-ball stats**  
- Use **Deep Learning** for player-level performance prediction  
- Build a **real-time match predictor web app** with UI

---

## 🛠️ How to Run

### ▶️ Option 1: Run on Google Colab
1. Open the notebook: [`IPL_MATCH_PREDICTION_2025.ipynb`](https://github.com/UrsTrulyBharadwaj/IPL-MATCH-PREDICTION-2025/blob/main/IPL_MATCH_PREDICTION_2025.ipynb)
2. Upload the required datasets in the runtime.
3. Execute the cells step-by-step.

### 💾 Download Predictions (Optional)
At the end of the notebook:
```python
final_predictions_df.to_excel("IPL_2025_Predictions.xlsx", index=False)
from google.colab import files
files.download("IPL_2025_Predictions.xlsx")

## 👨‍💻 Credits

- **Project By:** *Bharadwaj Atmakuri*  
- **Course:** *MBA Business Analytics (JNTU)*  
- **Tools Used:** *Python, Pandas, Scikit-learn, XGBoost, Matplotlib, Google Colab*  
- **Dataset Sources:** *Kaggle IPL Data, Custom 2025 Schedule*  
- **Guided By:** *ChatGPT (Prompt Engineering + ML Support)*  
- **Inspired By:** *IPL Fans, Cricket Analytics & Data Science Enthusiasts* 🌟  
- **GitHub:** [@UrsTrulyBharadwaj](https://github.com/UrsTrulyBharadwaj)  
- **Contact:** [itsbharadwajatmakuri@gmail.com]
