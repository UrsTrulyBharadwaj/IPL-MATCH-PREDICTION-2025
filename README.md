# 🏏 IPL 2025 Match Outcome Prediction
This project is a **Machine Learning-based system** designed to predict the outcome of IPL 2025 matches using historical data, team stats, venue records, toss decisions, and player auction insights.


# Objectives

To build a predictive model that takes into account:
- Team strengths
- Head-to-head statistics
- Toss decisions (Bat/Field)
- Venue and city-based records
- Recent form & win percentages

And outputs the **probable winner** of an IPL match.

## Datasets Used

- **Historical IPL Match Data (2010–2024)**  
- **IPL 2025 Schedule Data (from ESPNcricinfo or Kaggle)**  
- **Player Auction Stats (2025)**  

All datasets were in CSV/Excel format and combined after preprocessing.

## Feature Engineering

We derived the following key features:

- Team strength (based on player auctions)
- Recent form (last 3–5 match win rates)
- Venue win percentage (home/away performance)
- Toss result & decision impact
- Head-to-head record between teams
- City-specific performance (chasing/batting first trends)
- Net run rate differential

These were merged into the main dataset to improve model input quality.

## Machine Learning Models

We implemented and evaluated:

- **Logistic Regression**  
- **Random Forest Classifier**  
- **XGBoost Classifier (with tuning)**  
- **Voting Classifier (Ensemble of the above)**  


## Model Evaluation & Accuracy

| Model                | Accuracy | F1-Score |
|---------------------|----------|----------|
| Logistic Regression | 56.0%    | 49.8%    |
| Random Forest       | 52.1%    | 46.2%    |
| XGBoost (Tuned)     | 54.4%    | 50.2%    |


## Final Model Selection

After evaluating multiple models and performing hyperparameter tuning, **XGBoost** emerged as the most **balanced and reliable** model for match outcome prediction.

> "Although Logistic Regression showed slightly better raw accuracy at one point, XGBoost consistently delivered better overall balance in precision, recall, and F1-score. Hence, it was finalized for prediction deployment."

---

## ⚠️ Known Issues & Challenges

- Cricket outcomes are influenced by live/in-game dynamics not available pre-match.
- Recent player injuries, weather, or pitch conditions aren't part of current feature set.
- Slight overfitting in ensemble models (Voting Classifier).


## 🔭 Future Scope

- Add live player-level data (strike rate, economy, etc.).
- Integrate pitch and weather data via APIs.
- Try advanced models like LSTM for sequence predictions.
- Real-time updates during matches using streaming data.


## 🧪 How to Run This Project

1. Clone the repository  
2. Install requirements  
3. Run `ipl_match_prediction_2025.ipynb` in Google Colab or Jupyter Notebook  
4. Upload your datasets (CSV/Excel)  
5. The notebook will preprocess, train models, and output predictions



## 👨‍💻 Credits

- **Project By:** Bharadwaj Atmakuri  
- **Tools Used:** Python, Pandas, Scikit-learn, XGBoost, Google Colab  
- **Guided By:** ChatGPT (Prompt Engineering and ML Guidance)  
- **Inspired By:** IPL fans and data science enthusiasts 🌟



## 📎 License

MIT License. Free to use and modify.

