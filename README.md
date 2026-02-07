# Super Bowl LX Predictive Analytics: A Performance-Adjusted Win Probability Model for Seattle Seahawks VS New England Patriots

🏈 Executive Summary
In professional sports analytics, using full-season averages to predict a single game is a common pitfall—it ignores team momentum and introduces "look-ahead bias." This project engineered a Rolling Efficiency Model to predict the winner of Super Bowl LX. By evaluating teams based strictly on the data available entering the game, the model simulates a real-world sportsbook or front-office environment.

The Result: The model identifies a significant efficiency gap, predicting a definitive winner based on defensive-to-offensive point differentials.

🥁 AND THE WINNER IS...

The model has analyzed 50,000+ data points from the 2025 NFL Season.

Drumroll please... 🥁

🏆 SEATTLE SEAHAWKS 🏆

<img width="640" height="360" alt="image" src="https://github.com/user-attachments/assets/94d0fab6-95d8-4c87-9d2b-bdeaa3ab1368" />


Predicted Win Probability: 60.7% The New England Patriots trail with a 39.3% probability.

📈 Executive-Driven Questions I solved:

1. How do we objectively measure a team’s current strength without using "future" season averages that cause data leakage?

2. Which specific game phase (Seattle’s Offense vs. New England’s Defense) acts as the primary statistical anchor for the Super Bowl outcome?

The Verdict: Based on 2025 performance trends, what is the mathematically sound win probability for both finalists?


📊 **Key KPIs
Win Probability:** 60.7% (Seattle) vs. 39.3% (New England).

Feature Importance: Overall Point Differential was the #1 predictor of outcome.

Model Baseline Accuracy: 54.5% (Validated against 2025 regular-season volatility).


🛠 **Tech Stack & Methodology**
Data Source: nfl_data_py (Play-by-play data, >50,000 records).


Phase 1: ETL & Cleaning (SQL/Python): * Engineered Expanding Rolling Averages (expanding().mean()) to ensure no data leakage. Each game's features are calculated using only data from prior weeks.


Phase 2: Predictive Modeling (Python):

Implemented a Logistic Regression classifier.

Features: Matchup Differentials (Home Offense vs. Away Defense) and Overall Efficiency Gaps.


Phase 3: Insights & Storytelling:

Visualizing the probability spread and feature coefficients to explain the "Why" to stakeholders.


**🖼 Data Visualizations**
1. The Win Probability Gap
This chart shows the probability distribution between the Seahawks and the Patriots. ! 
<img width="984" height="583" alt="image" src="https://github.com/user-attachments/assets/f23f5707-5396-43cc-a423-68e689328f73" />

2. Feature Importance (The "Why")
Which metrics actually decided the game? The model heavily favored 'Overall Point Differential' over 'Home Field Advantage'. !
<img width="984" height="583" alt="image" src="https://github.com/user-attachments/assets/166a83de-6995-495d-bec0-05a8f7e8354e" />


**💡 Strategic Recommendations**
Exploit the Defensive Trend: Seattle’s win probability is driven by a late-season surge in offensive efficiency. Analysts should look for New England to struggle if they cannot disrupt Seattle’s early-down passing rhythm.

Refine the Model: Future iterations should incorporate Turnover Margin and Red Zone Efficiency as rolling metrics to further separate "lucky" wins from sustainable team performance.


**📂 Project Structure**
NFL_Super_Bowl_Winner.ipynb: The full data pipeline, from ingestion to prediction.

/visualizations: High-res exports of model insights for stakeholders.

/data: (Note: Data is fetched via API; script handles all ETL).
