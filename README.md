# 🎓 Student Performance Prediction — End-to-End ML Project

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-Web%20App-black?style=for-the-badge&logo=flask)
![ML](https://img.shields.io/badge/ML-XGBoost%20%7C%20CatBoost%20%7C%20RandomForest-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📌 Project Overview

An **end-to-end Machine Learning web application** that predicts a student's **Math score** based on their demographic background, parental education, lunch type, and test preparation status.

Built with **Python + Flask** for the web interface, and trained using multiple regression models including **XGBoost, CatBoost, and RandomForest** with **GridSearchCV** for hyperparameter tuning. Follows a clean **modular ML pipeline** architecture.

---

## ✨ Features

- 🔮 **Real-time Math Score Prediction** based on 7 input features
- 👤 **Demographic + Academic inputs** — gender, ethnicity, parental education, lunch, test prep
- 🤖 **Multiple ML Models** — XGBoost, CatBoost, RandomForest, and more compared
- ⚙️ **GridSearchCV** — best model auto-selected
- 🌐 **Flask Web UI** — simple form-based prediction interface
- 📦 **Modular Pipeline** — separate train & predict pipelines
- 📝 **Logging & Exception Handling** — production-grade structure

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Backend | Python, Flask |
| ML Models | XGBoost, CatBoost, RandomForestRegressor, and more |
| Model Selection | GridSearchCV (scikit-learn) |
| Data Processing | Pandas, NumPy, StandardScaler |
| Visualization | Matplotlib, Seaborn |
| Serialization | dill |
| Packaging | setuptools |

---

## 📁 Project Structure

```
student-performance-prediction/
│
├── app.py                         # Flask app — routes & prediction trigger
├── requirements.txt               # All dependencies
├── setup.py                       # Package setup
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py      # Load & split dataset
│   │   ├── data_transformation.py # Encoding, scaling, preprocessing
│   │   └── model_trainer.py       # Train & compare multiple models
│   │
│   ├── pipeline/
│   │   ├── train_pipeline.py      # End-to-end training pipeline
│   │   └── predict_pipeline.py    # Customdata class + Predictionpipeline
│   │
│   ├── logger.py                  # Logging configuration
│   ├── exception.py               # Custom exception handler
│   └── utils.py                   # save_object, load_object, evaluate_models
│
├── templates/
│   ├── index.html                 # Home page
│   └── home.html                  # Prediction form + result
│
├── artifacts/                     # Saved model & preprocessor files
├── notebook/                      # EDA & model experimentation
├── logs/                          # Application logs
└── catboost_info/                 # CatBoost training logs
```

---

## 🧠 Input Features

| Feature | Type | Description |
|---|---|---|
| `gender` | Categorical | Male / Female |
| `race_ethnicity` | Categorical | Group A / B / C / D / E |
| `parental_level_of_education` | Categorical | High school / Bachelor's / Master's etc. |
| `lunch` | Categorical | Standard / Free or reduced |
| `test_preparation_course` | Categorical | Completed / None |
| `reading_score` | Float | Score in reading (0–100) |
| `writing_score` | Float | Score in writing (0–100) |

**🎯 Target Variable:** `math_score` — predicted Math exam score

---

## ⚙️ How It Works

```
User Input (7 features)
        ↓
data_transformation.py  →  Encoding + Scaling via preprocessor.pkl
        ↓
model_trainer.py  →  Multiple Regressors + GridSearchCV
        ↓
Best Model saved  →  model.pkl
        ↓
Predictionpipeline  →  Loads model.pkl + preprocessor.pkl
        ↓
Flask UI  →  Returns predicted Math Score
```

---

## 🚀 Installation & Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/angrajDEV/student_performance_prediction.git
cd student_performance_prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
python app.py
```

Open `http://localhost:5000` in your browser.

---

## 💡 Key Highlights

- 🔄 **Modular ML pipeline** — ingestion → transformation → training → prediction
- 🏆 **Multi-model comparison** — best regressor auto-selected via GridSearchCV
- 💾 **Artifact persistence** — model & preprocessor saved with `dill`
- 📝 **Custom logging & exception handling** — production-grade code structure
- 📓 **EDA Notebook** — exploratory data analysis before modeling

---

## 👨‍💻 Author

**Angraj Dewangan (Nimmu)**  
MCA — Data Science & Machine Learning  
Guru Ghasidas University, Bilaspur

[![GitHub](https://img.shields.io/badge/GitHub-angrajDEV-black?style=flat&logo=github)](https://github.com/angrajDEV)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/)

---

> ⭐ If you found this project useful, do give it a star!
