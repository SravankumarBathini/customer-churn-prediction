# 📦 Telecom Subscriber Churn Prediction & Sequential Ensemble Engine

## 🏢 Business Case Overview
This repository contains a production-grade **Advanced Sequential Ensemble Pipeline** engineered to forecast customer churn probabilities (`subscriber_churn_status`) for an enterprise telecom provider.

In modern telecommunications, customer retention is a critical driver of profitability. Randomly offering promotional discounts across a massive subscriber base drains marketing margins, while missing early turnover indicators leads to high-value revenue leaks. This engine resolves that conflict by identifying non-linear risk factors, catching over 95% of churn indicators, and providing calibrated probability tracking to maximize customer lifetime value.

---

## 🏗️ Systems Architecture Map
The application is built as a fully decoupled, version-controlled analytics pipeline:

1. **Class-Stratified Processing Layers:** Ingests raw data using the Rust-backed **Polars** engine and parses matrices via **PyArrow**. It isolates data through a strict stratified 80/20 train/test partition to maintain precise 5.00% class distribution weights.
2. **Synthetic Minority Equilibrium (SMOTE):** Combats severe data skew by applying synthetic nearest-neighbor mathematical interpolation to level the training dataset into a perfect 50/50 balance (152,000 resampled training rows).
3. **Sequential Boosting Assembly (XGBoost):** Deploys an array of 150 sequential weak learners optimized using **Logarithmic Loss (LogLoss)** probability curves to completely eliminate high-confidence forecasting blunders.
4. **Friction Analysis Topography:** Deciphers the inner mechanics of the boosting trees, outputting clear, gain-based variable weights for executive stakeholder transparency reviews.

---

## 🛠️ Repository Layout
```text
customer-churn-prediction/
├── data/                         # Hidden/Ignored Data Storage
├── docs/
│   └── ml_concept_guide.md       # Visual Layman Guide to Imbalance & Boosting
├── models/                       # Ignored Serialized Output Binaries
├── notebooks/
│   └── churn_prediction_engine.ipynb # Interactive Active Playground Notebook
├── README.md                     # Technical Operations Overview
└── requirements.txt              # Frozen Production Dependencies
```

---

## 🚀 Execution & System Deployment Guide
To execute this model pipeline on your local environment terminal, process these PowerShell scripts:

```powershell
# 1. Clone your repository framework and move inside the project directory
cd customer-churn-prediction

# 2. Re-establish your isolated package environment sandbox
python -m venv churn_env
.\churn_env\Scripts\Activate.ps1

# 3. Build the core architecture package dependencies in a single pass
pip install -r requirements.txt
```
