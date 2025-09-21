# Abalone Age Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zey-2/abalone_age_prediction/blob/main/process_abalone.ipynb)

This project predicts the age of abalone (a type of sea snail) based on physical measurements using machine learning regression models.

## Dataset

The dataset used is the Abalone dataset from the UCI Machine Learning Repository. It contains physical measurements of abalone and their corresponding number of rings, which is used to estimate age (Age = Rings + 1.5).

Features:

- **Sex:** M (Male), F (Female), I (Infant)
- **Length:** Longest shell measurement (mm)
- **Diameter:** Perpendicular to length (mm)
- **Height:** With meat in shell (mm)
- **Whole weight:** Whole abalone (grams)
- **Shucked weight:** Weight of meat (grams)
- **Viscera weight:** Gut weight after bleeding (grams)
- **Shell weight:** After being dried (grams)
- **Rings:** Number of rings (target variable)

## Installation

1. Clone this repository.
2. Create and activate the conda environment:

```bash
conda env create -f environment.yml
conda activate abalone-env
```

## Usage

1. Ensure the dataset is in the `abalone/` directory.
2. Open the `process_abalone.ipynb` notebook in Jupyter.
3. Run the cells in order to:
   - Load and explore the data
   - Preprocess the data (encode categorical features, scale)
   - Train KNN and Linear Regression models
   - Evaluate the models

## Models

- **K-Nearest Neighbors (KNN) Regression:** k=1 to 21
- **Linear Regression**

## Results before Standard Scaler

    - **KNN Regression (k=7):**

    - Mean Squared Error: 4.88
    - R² Score: 0.55

    - **Linear Regression:**
    - Mean Squared Error: 4.89
    - R² Score: 0.55

## Results after Standard Scaler

    - **KNN Regression (k=7):**
    - Mean Squared Error: 5.23 (poorer with scaling)
    - R² Score: 0.52

    - **Linear Regression:**
    - Mean Squared Error: 4.89
    - R² Score: 0.55

Note: The results indicate less than desired performance.
