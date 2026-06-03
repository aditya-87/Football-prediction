# ⚽ Premier League Match Predictor

A Machine Learning project that predicts the outcome of English Premier League matches using historical match data, advanced feature engineering, and multiple classification algorithms.

## 📌 Project Overview

This project analyzes Premier League matches from multiple seasons and predicts whether a match will result in:

- 🏠 Home Win (H)
- 🤝 Draw (D)
- ✈️ Away Win (A)

The system uses historical performance metrics, Elo ratings, team form, shooting statistics, discipline records, and league standings to generate predictions.

---

## 🎯 Objectives

- Build an end-to-end Machine Learning pipeline.
- Compare multiple classification algorithms.
- Generate predictions through a REST API.
- Provide a simple frontend interface for users.
- Evaluate model performance using Accuracy, F1 Score, and Cross Validation.

---

## 🏗️ Project Architecture

```text
pl_project5_improved/
│
├── stage1_data/
│   └── merged.csv
│
├── stage2_eda/
│   ├── eda.py
│   ├── clean_data.csv
│   └── plots/
│
├── stage3_features/
│   └── Feature Engineering
│
├── stage4_models/
│   ├── train_models.py
│   ├── models/
│   └── plots/
│
├── stage5_evaluation/
│   └── api.py
│
├── stage6_frontend/
│   ├── index.html
│   ├── css/
│   └── js/
│
└── Research Papers & Documentation
```

---

## 📊 Dataset

The model is trained using historical English Premier League match data.

### Dataset Characteristics

| Feature | Description |
|----------|-------------|
| Seasons Covered | 1998–2025 |
| Matches | ~9,800+ |
| Competition | English Premier League |
| Target Variable | Match Result (H, D, A) |

---

## 🔥 Feature Engineering

The project creates advanced football analytics features including:

### ⚡ Elo Ratings
- Home Elo Rating
- Away Elo Rating
- Elo Difference

### 📈 Team Form Metrics
- Goals Scored
- Goals Conceded
- Goal Difference
- Win Rate
- Points Per Game
- Clean Sheet Rate

### 🎯 Shooting Statistics
- Shots on Target
- Total Shots
- Shot Accuracy

### 🚩 Set Piece Statistics
- Corners Won
- Corners Conceded

### 🟨 Discipline Statistics
- Yellow Cards
- Team Aggression Metrics

### 🏆 League Position Features
- Current League Position
- Season Points
- Goal Difference
- Position Gap
- Points Gap

---

## 🤖 Machine Learning Models

The project compares six algorithms from the Machine Learning syllabus.

| Algorithm | Category |
|------------|----------|
| Decision Tree | Tree-Based Learning |
| K-Nearest Neighbors (KNN) | Instance-Based Learning |
| Random Forest | Ensemble (Bagging) |
| AdaBoost | Ensemble (Boosting) |
| Support Vector Machine (SVM) | Margin-Based Learning |
| Naive Bayes | Probabilistic Learning |

---

## 🚀 REST API

The Flask backend exposes prediction endpoints.

### Start API

```bash
cd stage5_evaluation
python api.py
```

Server runs on:

```text
http://localhost:5000
```

### Available Endpoints

#### Health Check

```http
GET /health
```

#### Available Teams

```http
GET /teams
```

#### Model Information

```http
GET /models
```

#### Feature List

```http
GET /features
```

#### Single Model Prediction

```http
POST /predict
```

#### All Model Predictions

```http
POST /predict_all
```

#### Consensus Prediction

```http
POST /consensus
```

---

## 💻 Frontend

The project includes a browser-based frontend that allows users to:

- Select Home Team
- Select Away Team
- View model predictions
- Compare all algorithms
- View consensus prediction

To launch:

```bash
cd stage6_frontend
open index.html
```

or simply open the file in your browser.

---

## 📈 Evaluation Metrics

Models are evaluated using:

- Accuracy Score
- F1 Score
- Macro F1 Score
- Cross Validation
- Confusion Matrix

---

## 🛠️ Tech Stack

### Programming Language

- Python

### Machine Learning

- Scikit-Learn
- NumPy
- Pandas

### Data Visualization

- Matplotlib
- Seaborn

### Backend

- Flask
- Flask-CORS

### Frontend

- HTML
- CSS
- JavaScript

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/premier-league-match-predictor.git
cd premier-league-match-predictor
```

Install dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn flask flask-cors
```

---

## ▶️ Running the Project

### Step 1: Data Preparation

```bash
cd stage2_eda
python eda.py
```

### Step 2: Feature Engineering

```bash
cd stage3_features
python feature_engineering.py
```

### Step 3: Train Models

```bash
cd stage4_models
python train_models.py
```

### Step 4: Start API

```bash
cd stage5_evaluation
python api.py
```

### Step 5: Open Frontend

Open:

```text
stage6_frontend/index.html
```

in your browser.

---

## 📚 References

The project is supported by research and literature including:

- Random Forests
- XGBoost: A Scalable Tree Boosting System
- Scikit-Learn Documentation
- Soccer Outcome Prediction Research

---

## 🎓 Academic Purpose

This project was developed as part of a Machine Learning academic project and demonstrates:

- Data Preprocessing
- Exploratory Data Analysis
- Feature Engineering
- Supervised Learning
- Model Evaluation
- API Development
- Frontend Integration

---

## 👨‍💻 Author

**Aditya Yadav**

Software Engineering Student

---

## ⭐ If you found this project useful

Please consider starring the repository to support the project.
