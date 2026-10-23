# Waste Management & Recycling in Indian Cities - Hackathon Project

## Overview
This project was created for the **Mini Hackathon: Waste Management & Recycling in Indian Cities**.  
Our goal: **Predict Recycling Rate** using machine learning models trained on landfill and recycling center data.  
By analyzing waste patterns, municipalities can **optimize collection schedules**, **reduce overflow**, and **improve recycling efficiency**.

---

## Dataset Overview
- **Source:** Provided hackathon dataset  
- **Rows:** 851
- **Columns:** Multiple numerical and categorical features (e.g., waste type, location, landfill name, disposal method)
- **Target Variable:** Recycling Rate
- **Cleaning Steps:**
  - Splitted the column "Landfill Location (Lat, Long)"
  - Encoded categorical columns (`Waste Type`, `District/City`, etc.)
  - Removed non-numeric columns from modeling

---

## Project Structure

```
project_root/
│
├── data/
│ ├── raw/ # Raw dataset file
│ ├── processed/
│    ├── processed file
│
├── Notebooks/
│ ├── exploratory_data_analysis.ipynb # Exploratory Data Analysis
│ ├── data_preparation.ipynb # Data cleaning & encoding
│ ├── model_training.ipynb # Model training & evaluation
│
├── models/ # Saved trained models
├── app.py # Flask app
├── templates/index.html # Web UI
├── metrics.json # Model scores
├── Predictions/predictions.csv
├── Report.pdf # Generated summary report
├── README.md # This file
└── requirements.txt # Python dependencies
```

### Installation & Usage

1. Install Dependencies:
```bash
pip install -r requirements.txt
```

2. Run Jupyter Notebooks (EDA, training):
```bash
jupyter notebook
```

3. Run Flask App:
```bash
python app.py
```

Visit: http://127.0.0.1:5000

---

## Model Performance

| Model            | RMSE    |
| ---------------- | ------- |
| LinearRegression | 17.5686 |
| RandomForest     | 17.6317 |
| XGBoost          | 19.1556 |
| LightGBM         | 19.0014 |

Selected Best Model: LinearRegression

---

## Reports & Artifacts

- `Report.pdf` – Model summary, dataset analysis, and insights.
- `metrics.json` – Cross-validation RMSE metrics.
