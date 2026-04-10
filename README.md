# Spotify Tracks Data Analysis

An end-to-end **Exploratory Data Analysis (EDA)** and **Machine Learning** project on a Spotify tracks dataset. The project uncovers patterns in audio features such as popularity, energy, danceability, tempo, valence, and more — and builds predictive models to estimate song popularity.

---

## Project Overview

This project investigates what makes a song popular on Spotify by analyzing audio characteristics across ~114,000 tracks. It combines statistical exploration, data visualization, and machine learning to draw meaningful insights from the data.

---

## Dataset

- **Source:** Spotify Tracks Dataset (CSV inside a ZIP archive)
- **Size:** ~114,000 songs, 20 features
- **Key Features:** `popularity`, `energy`, `danceability`, `tempo`, `valence`, `acousticness`, `instrumentalness`, `liveness`, `speechiness`, `loudness`, `duration_ms`

---

## Project Structure

```
├── Spotify_eda_project.ipynb   # Main Jupyter Notebook
├── archive.zip                 # Compressed dataset
├── dataset.csv                 # Extracted dataset (after running the notebook)
└── README.md
```

---

## Data Cleaning

- Removed **1 row** with missing values
- Found **no duplicate rows**
- Dropped the unnecessary `Unnamed: 0` index column
- Converted `duration_ms` to minutes for easier interpretation
- Final cleaned dataset: **113,999 rows × 20 columns**

---

## Exploratory Data Analysis

### Popularity Distribution
- Scores range from **0 to 100**, with a mean of **33.32** and median of **35**
- 50,486 songs → Low popularity (< 30)
- 58,041 songs → Moderate popularity (30–69)
- 5,472 songs → High popularity (≥ 70)

### Audio Feature Insights

| Feature | Mean | Key Finding |
|---|---|---|
| Energy | 0.642 | Songs lean toward mid–high energy |
| Danceability | 0.567 | Most songs are moderately danceable |
| Valence (mood) | 0.474 | Evenly split between happy and sad tones |
| Tempo | 122.17 BPM | Centered around typical song speeds |
| Duration | 3.80 min | Most songs fall near the standard range |

### Popular vs Non-Popular Songs
Songs in the **top 25% popularity** were compared against the rest to see which audio features differentiated them. Findings showed only weak differences across most features, reinforcing that no single characteristic drives popularity.

### Correlation Analysis
A heatmap revealed that individual audio features have **weak correlations with popularity**, suggesting that song success is shaped by a combination of factors.

---

## Machine Learning Models

Nine audio features (`danceability`, `energy`, `loudness`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`) were used to predict song popularity.

**Train/Test Split:** 80% training / 20% testing

| Model | R² Score |
|---|---|
| Linear Regression | Baseline (low) |
| K-Nearest Neighbors | Moderate |
| XGBoost | Moderate |
| **Random Forest** | **Best (~0.531)** |

**Random Forest** emerged as the best model, though its moderate R² score confirms that audio features alone are insufficient to fully predict popularity.

### Feature Importance (Random Forest)
The most influential features were **acousticness** and **tempo**, though no single feature dominated, further highlighting that popularity is multi-dimensional.

---

## Key Takeaways

- Song popularity is **not driven by any single audio feature**
- Most songs are moderately energetic, danceable, and average in tempo
- Advanced ML models outperform Linear Regression but still achieve only moderate accuracy
- External factors like **artist reputation, marketing, and release timing** likely play a significant role in a song's success
- For artists: success comes from a **balanced combination** of musical elements, not maximizing one trait

---

## Tech Stack

- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib & Seaborn** — data visualization
- **Scikit-learn** — ML models (Linear Regression, Random Forest, KNN)
- **XGBoost** — gradient boosting model

---

## Contact

Feel free to reach out or raise an issue if you have suggestions or questions!
Riva Chaudhary
