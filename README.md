⚡ Lightning Forecasting System

A Machine Learning–based early warning tool for predicting lightning risk in Jharkhand, India.
Lightning have immediate and long-term effects on people, structures and the environment,
resulting in deaths, severe injuries and property damage. Lightning is a frequent occurrence
with an estimated 50 occurrence per second. Jharkhand, in particular, is experiencing an
increase in the number of deaths due to lightning strikes. It is estimated that 431 people have
lost their lives in the 2025 monsoon period. Along with people, many animals have also lost
their lives. Out of all the states in India, Jharkhand is one of the six states highly prone to
lightning deaths. In the annual report of Climate Resilient Observation System Promotion
Council (CROPC), 1669 people have died in Jharkhand due to lightning strikes with an
average of 436,250 lightning strikes in last five years. To prevent this from happening, we
should have a Lightning Prediction System, to prevent from these casualties and damage. A
good Lightning Prediction System can save crores of the Government from structural
damages and also save millions of lives, not only in Jharkhand but all across the world.

📌 Project Overview

Lightning strikes have become a growing threat in Jharkhand, leading to casualties, loss of livestock, and damage to property.
This project aims to build a data-driven Lightning Forecasting System that predicts lightning probability using:

LIS (Lightning Imaging Sensor) satellite lightning occurrence data

MTS (Meteorological Time Series) district-wise weather data

Engineered atmospheric features

Machine Learning ensemble models

📁 Features
✔ Machine Learning Ensemble Model

The final prediction is based on the average probability from:
Logistic Regression
Multi-Layer Perceptron (MLP)
Gradient Boosting

✔ Key Weather Inputs
Temperature
Relative Humidity
Rainfall
Wind Speed
Surface Pressure
3-day rolling features
Pressure drop
District spatial encoding



🛠 Tech Stack

Python

Pandas, NumPy

Scikit-learn

Imbalanced-learn (SMOTE)

Matplotlib / Seaborn for evaluation


🧠 Machine Learning Approach

1. Data Preprocessing
Missing-value handling
Duplicate removal
Unnamed column cleanup
Merge of LIS + MTS datasets

2. Feature Engineering
Generated new atmospheric features:
Heat Index (THI)
Pressure Drop
3-day rolling means
Rainfall category
Season encoding
District one-hot encoding
Calendar features (Month, DOY, Week)

3. Data Balancing
Used SMOTE–Tomek Links to handle extreme class imbalance
(lightning days are very rare).

4. Model Training
Evaluated models:
Logistic Regression
Random Forest
XGBoost
Gradient Boosting
Multi-Layer Perceptron (MLP)
Final ensemble = LR + MLP + Gradient Boosting


📌 Folder Structure
Lightning_Prediction_System/
│
├── Processed_Districts                      
├── Snapshots
├── lightning_dataset_FE_v2
├── lightning_ensemble_model.pkl 
├── lightning_gb_calibrated.pkl 
├── lightning_rf_model.pkl 
├── LightningPrediction
├── LightningPredictionReport
├── requirements.txt             
└── README.md                   

⚙ Installation (Run Locally)
Clone the repo:
git clone https://github.com/Priyangshu22/Lighting-Prediction-System.git
cd Lightning-Forecasting-System

Install dependencies:
pip install -r requirements.txt


📌 Future Scope

Replace SMOTE with ADASYN or Borderline SMOTE

Hyperparameter tuning using Optuna

Time-series version of lightning prediction

Integration with real-time weather API

Dataset expansion for higher recall


📚 References

LIS Satellite Lightning Data
MTS District-level Weather Data
SMOTE & Tomek Links (Imbalanced-learn)
Scikit-learn ML Documentation
Research on lightning detection & atmospheric patterns

🙋‍♂️ Author

Priyangshu Paul
MCA-Bira Institute of Technology,Mesra
Github: @Priyangshu22


Shubham Kumar
MCA – Birla Institute of Technology, Mesra
GitHub: @shubham0745

⭐ Show Your Support

If this project helped you or you found it interesting:

👉 Star ⭐ the repository
👉 Use it in your resume / LinkedIn

