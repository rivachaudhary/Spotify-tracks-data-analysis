# Spotify Data Analysis & Popularity Prediction

## Overview
This project performs end-to-end data analysis on a Spotify dataset to understand music trends and predict song popularity using machine learning.

It focuses on exploring relationships between audio features and identifying patterns that influence a track’s popularity.

---

## Dataset
The dataset contains Spotify track features such as:
- Popularity
- Danceability
- Energy
- Loudness
- Tempo
- Acousticness
- Valence
- Speechiness

---

## Project Workflow

### 1. Data Cleaning
- Removed missing values
- Checked and handled duplicates
- Cleaned unnecessary columns

### 2. Exploratory Data Analysis (EDA)
- Analyzed distribution of popularity
- Visualized feature relationships
- Created correlation matrix to understand dependencies

### 3. Machine Learning Models
- Linear Regression
- K-Nearest Neighbors
- Random Forest
- XGBoost

### 4. Model Evaluation
- Compared models using:
  - R² Score
  - Mean Squared Error (MSE)
- Evaluated performance differences between linear and non-linear models

---

## Key Insights
- Song popularity is influenced by multiple features, not just one
- Relationships between features and popularity are mostly non-linear
- Random Forest performed best among all models
- Simple linear models were not sufficient to capture complex patterns

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Project File
- `Spotify_eda_project.ipynb`

---

## How to Run
1. Open the notebook in Google Colab or Jupyter Notebook  
2. Run all cells sequentially  
3. Explore outputs, visualizations, and model results  

---

## Future Improvements
- Add more features such as artist popularity or followers  
- Try advanced models for better prediction  
- Improve feature engineering  

---

## Author
Riva Chaudhary
