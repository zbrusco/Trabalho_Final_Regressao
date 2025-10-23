# 🩺 Predictive Analysis of Health Insurance Costs

![Language](https://img.shields.io/badge/Language-R-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

This repository contains the **final project for the course Introduction to Data Science with R**.  
It develops a **multiple linear regression model** to predict health insurance costs based on demographic and lifestyle factors.

---

## Table of Contents
- [📖 Project Overview](#project-overview)
- [🎯 Objective](#objective)
- [🗂️ Dataset](#dataset)
- [🔎 Methodology](#methodology)
- [📊 Key Findings](#key-findings)
- [⚙️ How to Run](#how-to-run)
- [👨‍💻 Authors](#authors)
 
---

## Project Overview

Developed as the final assessment for the **Introduction to Data Science** course, this project applies all stages of a data science workflow — from data cleaning and exploration to modeling, validation, and communication of results.

---

## Objective

To measure how demographic and lifestyle variables impact health insurance costs.  
The analysis evolved from a general linear regression model to a **segmented approach**, modeling smokers and non-smokers separately for better cost prediction accuracy.

---

## Dataset

The study uses the public **"Medical Cost Personal Datasets"** from Kaggle.

- **Source:** [Kaggle - Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)  
- **Observations:** 1,338  
- **Main Variables:**  
  - `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges` (target variable)

---

## Methodology

1. **Exploration & Preprocessing:** Initial data exploration and log transformation of `charges` to handle skewness.  
2. **General Model:** Initial multiple regression achieved **Adjusted R² = 74.4%**, but residual analysis showed heteroskedasticity.  
3. **Segmented Models:**  
   - One model for **non-smokers**.  
   - One **interaction model** for **smokers**, accounting for combined risk factors.

---

## Key Findings

### Non-Smokers
- **Adjusted R² = 0.686**  
- Costs show a moderate, predictable pattern.  
- Key predictors: `age`, `children`, and `region`.  
- BMI had limited isolated impact.

### Smokers
- **Adjusted R² = 0.914**  
- Costs are higher and more volatile.  
- **Main finding:** The combination of **smoking, obesity (BMI ≥ 30), and age** exponentially increases costs.

---

## How to Run

### 1. Requirements
- **R** (v4.0+)  
- **RStudio**

### 2. Installation
Clone the repository:
```bash
git clone https://github.com/zbrusco/health_cost_analysis
```

---

## Authors

- [Andre Loureiro Montini Ferreira](https://github.com/jfandre00)
- [Lucas Amorim Brusco](https://github.com/zbrusco)
- [Pedro Conceição Costa](https://github.com/dev-pedr0)
- [Marcelo De Azevedo Sampaio](https://github.com/marcelosampaio)
- [Kauan Lima Oliveira](https://github.com/devKauanLima)

---
