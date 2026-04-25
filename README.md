# Online-Game-Popularity-Prediction
End-to-end ML pipeline to predict game popularity (RecommendationCount) using structured data. Includes preprocessing, feature engineering, feature selection (ANOVA, MI, Lasso), and regression models (Linear, Polynomial Ridge, SVR). Evaluated with R², RMSE, MAE using K-Fold cross-validation.

🚀 Project Overview
The goal is to predict how popular a game will be based on features such as:
Player statistics (SteamSpy data)
Game metadata (price, release date, achievements)
Platform and feature indicators
The workflow follows a real-world ML pipeline:
Data cleaning & preprocessing
Feature engineering
Feature selection
Model training & tuning
Evaluation & visualization

🧹 Data Preprocessing
Key preprocessing steps include:
Handling missing values and duplicates
Converting ReleaseDate into numerical format
Encoding boolean features into numeric values
Dropping high-null or irrelevant columns
Extracting useful features (e.g., number of supported languages)

🔍 Feature Selection
Multiple techniques were used to identify the most impactful features:
Correlation analysis
ANOVA (F-test)
Mutual Information
Lasso Regression
Final selected features include:
SteamSpyOwners, SteamSpyPlayersEstimate
Metacritic, AchievementCount
PriceInitial, ReleaseDate
and other key predictors

📊 Models Used
The following regression models were implemented and compared:
Linear Regression
Polynomial Regression (with Ridge regularization)
Support Vector Regression (SVR - RBF kernel)

⚙️ Model Evaluation
Models are evaluated using:
R² Score
RMSE (Root Mean Squared Error)
MAE (Mean Absolute Error)
Cross-validation is performed using K-Fold (k=5) for reliable performance estimation.

🔧 Hyperparameter Tuning
Ridge regularization strength (alpha) is optimized
SVR parameters (C, epsilon) are tuned

📈 Visualization
The project includes:

Feature correlation plots
Scatter plots with trendlines (log-scaled)
Regression prediction vs actual plots
🧠 Key Highlights
End-to-end ML pipeline implementation
Combination of multiple feature selection techniques
Use of log transformation to stabilize target variable
Model comparison with proper validation


🛠️ Tech Stack
Python
NumPy, Pandas
Scikit-learn
Matplotlib, Seaborn, Plotly
