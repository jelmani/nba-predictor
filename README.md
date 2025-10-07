# nba-predictor

## About the project
This project is part of my journey through Andrew Ng’s Machine Learning Specialization, where I build a capstone project for each section.
Here, I applied multiple linear regression and vectorization to predict how many points an NBA player will score in a given game — based on stats from previous games and opponent data.

## Overview

The goal was to predict points scored by a player using multiple input features such as:

- Rolling averages of last 5 games (points, minutes, field goals attempted, etc.)

- Days of rest before the game

- Opponent stats (pace, defensive rating, etc.)

The project focuses on:

- Building a reusable, modular data preprocessing pipeline

- Implementing multiple linear regression from scratch (no sklearn)

- Practicing vectorization and feature scaling for performance

## Key Concepts

- Vectorization: replaced slow loops with efficient NumPy operations and matrix math

- Feature Engineering: experimented with rolling averages, rest days, and opponent metrics

- Z-Score Normalization: applied to all features for faster gradient descent convergence

- Cost Function & Gradient Descent: manually implemented to train model parameters
- Regularization: used to increase accuracy of model

## How it works
### Data Collection
1. Data is sourced from Basketball Reference. CSVs are processed to create training, validation, and test sets.

### Feature Engineering
2. Rolling averages are computed using Pandas’ rolling() and shift() functions to exclude the current game from averages.

### Model Training
3. Multiple Linear Regression trained using gradient descent and vectorized operations.

### Evaluation
4. Model tested on 2024 season data and compared against baseline performance (mean points scored).

## Results

The model’s cost was slightly higher than the standard deviation of the target data — meaning it didn’t outperform the baseline yet.
Possible reasons include feature quality, data leakage, or the limits of linear regression for this task.

Despite that, the project was a great exercise in:

- Feature engineering
- Vectorized computation
- Understanding model limitations with real-world data

## Next Steps

- Add polynomial features
- Experiment with regularization
- Try non-linear models (tree-based or neural nets)
- Improve opponent-based features (season-to-date instead of full-season averages)

