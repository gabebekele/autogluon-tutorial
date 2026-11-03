# Learn AutoGluon in 60 Minutes: NYC Airbnb Prices

A tutorial for ML students: learn AutoGluon's tabular regression API by building and evaluating an NYC Airbnb nightly-price predictor. Adapted from a separate portfolio ML project.

## Contents
- `autogluon.API.ipynb`: what AutoGluon does, the core APIs, and a self-contained toy demonstration.
- `autogluon.example.ipynb`: end-to-end Airbnb model training, controlled Linear Regression comparison, pricing analysis, learning checks.
- `requirements.txt`: Python dependencies.

## Learning outcomes
Explain `TabularPredictor`, `.fit()`, `.predict()`, `.evaluate()`, `.leaderboard()` and `.feature_importance()`; implement a reproducible train/test split; interpret regression error; compare a baseline on equivalent features.

## Dataset
Download [New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data) and save the CSV to `data/AB_NYC_2019.csv` (not committed). The tutorial reproduces the portfolio's cleaning filters but **intentionally uses unscaled raw features for AutoGluon**; therefore numerical results may differ from the portfolio experiment.

## Install and run
Use Python 3.11 in a fresh environment, install dependencies from `requirements.txt`, and open the notebooks in VS Code/Jupyter. Start with `autogluon.API.ipynb`, then `autogluon.example.ipynb`. The example trains **two separate AutoGluon predictors**; adjust `TRAINING_TIME_LIMIT` for your machine. AutoGluon stores training artifacts under `AutogluonModels/`.

## Methods
- 80/20 seeded train/test split following data filters
- Original AutoGluon regression with title text
- Controlled AutoGluon without title text vs scikit-learn Linear Regression
- MAE, RMSE, R², leaderboard, and permutation feature importance
- Descriptive borough/room-type and title-amenity exploration

## Important limitations
Results vary with training budget and software/hardware; the dataset represents filtered 2019 listings, not current prices; title keywords are not verified amenities. The tutorial does not contain hard-coded performance claims. Do not treat the test set as a validation set when tuning.

## Class submission
Place these files **inside the instructor-prescribed course project directory** and follow the official `class_project/project_template` for Docker scripts, repository naming, issue and pull request workflow. Docker is **not yet configured or verified** in this first teaching draft. The assignment also requires a 10–20 minute video walkthrough.
