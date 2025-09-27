## END End Machine Learning Project

# Student Performance Prediction ML Project 🎓

![Python](https://img.shields.io/badge/Python-3.9–3.11-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2.2-green)
![CatBoost](https://img.shields.io/badge/CatBoost-Regression-orange)
![Status](https://img.shields.io/badge/Project-Active-success)

---

## Table of Contents

* [Project Overview](#project-overview)
* [Features](#features)
* [Dataset](#dataset)
* [Installation](#installation)
* [Usage](#usage)
* [Regression Models Used](#regression-models-used)
* [Evaluation Metrics](#evaluation-metrics)
* [Pipeline & Modularity](#pipeline--modularity)
* [Contributing](#contributing)
* [Contact](#contact)

---

## Project Overview

This project predicts student academic performance in **math, reading, and writing** using a **modular machine learning pipeline**.

Key highlights:

* **Feature Engineering & Preprocessing**:

  * Standard scaling of numeric features
  * One-hot encoding of categorical features using `ColumnTransformer`
  * Modular design ensures compatibility with multiple regression models
* **Regression Models**: CatBoostRegressor, XGBRegressor, RandomForestRegressor, AdaBoostRegressor, GradientBoostingRegressor, LinearRegression, DecisionTreeRegressor, KNeighborsRegressor
* **Evaluation**: R² score for each target variable
* **Deployment-ready**: Pipeline supports easy integration with Streamlit
* **Experiment Tracking**: Optional MLflow/DagsHub logging for metrics and models

---

## Features

* Modular, reusable pipeline for preprocessing, training, and prediction
* Automatic encoding and scaling for mixed-type features
* Supports multiple regression models for comparative evaluation
* Logs model performance metrics for easy comparison
* Ready for deployment as API or interactive UI

---

## Dataset

* Columns:

  * **Categorical features**: `gender`, `race_ethnicity`, `parental_level_of_education`, `lunch`, `test_preparation_course`
  * **Numeric targets**: `math_score`, `reading_score`, `writing_score` (0–100 range)
* Dataset is **already clean**; preprocessing handles encoding and scaling
* Suitable for regression modeling with all listed algorithms

---

## Installation

```bash
git clone https://github.com/your-username/student-performance-ml.git
cd student-performance-ml

python -m venv venv
# Activate virtual environment
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

---

## Usage

### Train Models

```bash
python train.py
```

* Preprocesses data with scaling & one-hot encoding
* Trains multiple regression models
* Evaluates R² scores for each target

### Predict on New Data

```python
from predict import predict_student_performance

sample_input = {
    "gender": "female",
    "race_ethnicity": "group B",
    "parental_level_of_education": "bachelor's degree",
    "lunch": "standard",
    "test_preparation_course": "completed"
}

predictions = predict_student_performance(sample_input)
print(predictions)
```

---

## Regression Models Used

* CatBoostRegressor
* AdaBoostRegressor
* GradientBoostingRegressor
* RandomForestRegressor
* LinearRegression
* KNeighborsRegressor
* DecisionTreeRegressor
* XGBRegressor

---

## Evaluation Metrics

* **R² score** for all numeric targets (`math_score`, `reading_score`, `writing_score`)
* Compare models to select best-performing regressor per target

---

## Pipeline & Modularity

```
[ Raw Dataset ]
        │
        ▼
[ Preprocessing Module ] → ColumnTransformer: scaling + one-hot encoding
        │
        ▼
[ Training Module ] → Train multiple regression models
        │
        ▼
[ Evaluation Module ] → Compute R² scores
        │
        ▼
[ Prediction Module ] → Predict on new inputs
```

* Modular design allows clean separation of preprocessing, training, evaluation, and prediction

---

## Contributing

1. Fork the repository
2. Create a branch: `git checkout -b feature-name`
3. Make changes & commit: `git commit -m "Add feature"`
4. Push: `git push origin feature-name`
5. Open a Pull Request

---

## Contact

* **Harshit Dubey**
* Email: [harshitdubey7896@gmail.com](mailto:harshitdubey7896@gmail.com)
* GitHub: [harshitdubey2001](https://github.com/harshitdubey2001)

```
  
