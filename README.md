# Lasso-Regression
## Feature Selection Using Lasso Regression

This repository contains the full seminar project “Feature Selection: Spotlight on Lasso Regression”, submitted as part of the M.Sc. (Statistics) program at The Maharaja Sayajirao University of Baroda. It combines statistical theory, mathematical foundations, and empirical demonstrations to explain how Lasso regression performs both regularization and automatic feature selection.

The project studies why ordinary least squares fails in high-dimensional settings, how regularization fixes this, and why Lasso is uniquely suited for building sparse, interpretable models.

## What This Project Covers

The work is structured around three core ideas:

### 1. Why regularization is needed
- Ordinary least squares suffers from high variance, overfitting, and instability when predictors are correlated or when the number of features is large 

### 2. How Lasso works
- Lasso introduces an L1 penalty on regression coefficients, which shrinks them and can force some of them to exactly zero. This allows Lasso to perform feature selection automatically while still fitting a predictive model 

### 3. Why Lasso is different from Ridge
- Ridge regression shrinks coefficients but never removes them. Lasso, because of the geometry of the L1 penalty, produces sparse solutions where irrelevant variables disappear from the model 

## Datasets Used

Two datasets are used to demonstrate the behavior of Lasso.

### 1. Simulated Experience–Salary Data

- A synthetic dataset is used to illustrate the bias–variance tradeoff. A simple linear model underfits, while a high-degree polynomial overfits. Lasso finds a middle ground by shrinking coefficients and improving generalization performance 

### 2. Diabetes Dataset

- A real dataset with 442 patients and 10 standardized predictors (age, BMI, blood pressure, and blood serum measurements) is used to show how Lasso performs feature selection. As the penalty parameter increases, weak predictors are eliminated while strong predictors such as BMI and blood pressure remain active 

## Feature Selection with Lasso

The key property that makes Lasso valuable is its ability to drive coefficients exactly to zero. This means:
- Unimportant variables are removed from the model
- Important variables remain with non-zero coefficients
- The resulting model is simpler and easier to interpret

In the diabetes dataset, increasing the regularization parameter progressively removes weaker features until only the strongest predictors remain, clearly demonstrating Lasso’s feature selection ability 

## Choosing the Regularization Parameter

The project compares several methods for selecting the Lasso penalty parameter λ:

- K-fold cross-validation (recommended for prediction)
- AIC and BIC (useful for model selection and explanation)
- Regularization path visualization

A practical workflow combining cross-validation and information criteria is also discussed to balance prediction accuracy and interpretability 

## Key Results

The experiments show that:
- Lasso successfully balances bias and variance
- It produces sparse, interpretable models
- It identifies meaningful predictors in real data
- It outperforms unregularized regression when many features are present

In the diabetes example, Lasso consistently identifies BMI, blood pressure, and selected serum measures as the most important variables, matching known medical relationships 

## Repository Contents

This repository includes:
- Seminar presentation slides
- Full written seminar report (PDF)
- Figures showing regularization paths and coefficient shrinkage
- Tables demonstrating how coefficients change with λ

Together, these provide both conceptual understanding and empirical evidence of how Lasso regression works.

## Academic Context

This work was submitted as an M.Sc. seminar project in Statistics and is based on the foundational work of Tibshirani (1996) and subsequent developments in regularized regression and feature selection
