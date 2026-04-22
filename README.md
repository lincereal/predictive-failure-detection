# 🔧 Predictive Failure Detection — NASA Turbofan

> Predicting Remaining Useful Life (RUL) of industrial 
> components using machine learning to enable preventive 
> maintenance before failures occur.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![XGBoost](https://img.shields.io/badge/XGBoost-ML-green)
![R2](https://img.shields.io/badge/R²-0.80-brightgreen)
![Status](https://img.shields.io/badge/Status-Complete-success)

---

## 📊 Results

| Metric | Value |
|--------|-------|
| R² Score | **0.8045** |
| MAE | **13.30 cycles** |
| RMSE | **18.38 cycles** |
| CV RMSE | **18.48 ± low variance** |
| Risk Zone Accuracy | **See notebook 04** |

> The model predicts component failure within a 13-cycle 
> window — actionable enough to schedule preventive 
> maintenance before failure occurs.

---

## 🎯 Business Context

This project mirrors real-world challenges faced in 
consumer electronics quality engineering:

- **At Sony Electronics**, failure patterns in TV product 
  lines were detected manually through field data analysis
- This model **automates that detection**, predicting 
  remaining useful life before failure occurs
- Enables maintenance teams to act **proactively** instead 
  of reactively

---

## 📁 Project Structure

predictive-failure-detection/
│
├── data/
│   ├── train_FD001.txt          # Raw training data
│   ├── test_FD001.txt           # Raw test data
│   ├── RUL_FD001.txt            # Ground truth RUL
│   ├── train_processed.csv      # Processed training data
│   └── test_processed.csv       # Processed test data
│
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb   # EDA & visualization
│   ├── 02_feature_engineering.ipynb    # RUL creation & scaling
│   ├── 03_model_training.ipynb         # XGBoost training & CV
│   └── 04_evaluation.ipynb             # Risk zones & dashboard
│
├── src/
│   ├── model/
│   │   └── xgboost_rul_model.pkl       # Trained model
│   ├── sensor_degradation.png
│   ├── rul_analysis.png
│   ├── model_evaluation.png
│   ├── feature_importance.png
│   └── final_dashboard.png
│
├── requirements.txt
└── README.md

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/lincereal/predictive-failure-detection
cd predictive-failure-detection

# Create virtual environment
python -m venv venv
venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt

# Run notebooks in order
# 01 → 02 → 03 → 04
```

---

## 🛠️ Tech Stack

- **Python 3.11**
- **XGBoost** — gradient boosting model
- **Scikit-learn** — preprocessing & evaluation
- **Pandas / NumPy** — data manipulation
- **Matplotlib / Seaborn** — visualization

---

## 📈 Key Visualizations

### Sensor Degradation Over Time
Tracks how 6 critical sensors degrade across engine cycles — 
the pattern that precedes failure.

### Risk Zone Classification
Engines classified into three actionable zones:
- 🟢 **NORMAL** — No action needed
- 🟡 **WARNING** — Schedule inspection  
- 🔴 **CRITICAL** — Immediate maintenance required

### Model Performance Dashboard
Final evaluation combining scatter analysis, error 
distribution, and business metrics in a single view.

---

## 👤 Author

**Aldo Yamil Avila Carrillo**  
Quality Engineer → ML Engineer  
4+ years at Sony & LG Electronics  
Master's in Artificial Intelligence

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](
https://linkedin.com/in/aldo-avila-carrillo/)
[![GitHub](https://img.shields.io/badge/GitHub-lincereal-black)](
https://github.com/lincereal)
