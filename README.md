# Predictive Analysis using ML Algorithms

This repository is a collection of three distinct machine learning projects ("assessments") focused on predictive analysis. The projects demonstrate the application of various supervised learning algorithms (both regression and classification) to solve specific, real-world data problems. All assessments strictly adhere to the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology, covering business understanding, data understanding, data preparation, modeling, evaluation, and deployment considerations.

---

## Table of Contents

1.  [Repository Structure](#-repository-structure)
2.  [Project Assessments Summary](#-project-assessments-summary)
    * [1. Assessment 01: Wine Quality Regression](#1-assessment-01-wine-quality-regression)
    * [2. Assessment 02: Wine Quality Classification](#2-assessment-02-wine-quality-classification)
    * [3. Assessment 03: Bike Share Demand Regression](#3-assessment-03-bike-share-demand-regression)
3. [Algorithms](#-algorithms)
4.  [Setup and Installation](#-setup-and-installation)
    * [Prerequisites](#prerequisites)
    * [Environment Setup](#environment-setup)
    * [Running the Projects](#running-the-projects)
5.  [License](#-license)
6.  [Contact](#-contact)

---

## Repository Structure

### The repository is organized to clearly separate the main project notebooks from the data and configuration files.
    predictive-analysis-using-ml-algorithms/ 
      ├── assessment_01.ipynb # Wine Quality Regression Project 
      ├── assessment_02.ipynb # Wine Quality Classification Project 
      ├── assessment_03.ipynb # Bike Share Demand Regression Project 
      ├── data/ # Directory for all source data files (Placeholder) │ 
        ├── winequality-red.csv │ 
        ├── winequality-white.csv 
        │ └── day.csv 
      ├── README.md # This file 
      ├── requirements.txt # All Python package dependencies 
      └── .gitignore # Configuration for files to ignore

---

## Project Assessments Summary

| File | Project Title | Problem Type | Primary Success Metric | Champion Models Explored |
| :--- | :--- | :--- | :--- | :--- |
| `assessment_01.ipynb` | **Wine Quality Regression** | Regression | MSE $< 0.40$ | XGBoost, LightGBM |
| `assessment_02.ipynb` | **Wine Quality Classification** | Classification | F1-Score $\ge 0.70$, AUC-ROC $\ge 0.75$ | Random Forest, XGBoost, MLP |
| `assessment_03.ipynb` | **Bike Share Demand Regression** | Regression | R² score $\ge 0.85$ | Gradient Boosting, Extra Trees, PCA-enhanced Models |

### 1. Assessment 01: Wine Quality Regression

* **Business Problem:** The need for a rapid, objective, and cost-effective quality control measure for red wine production to replace or augment slow human sensory tests.
* **Methodology Focus:** Rigorous data cleaning, including **Interquartile Range (IQR)** fences for outlier removal, and an in-depth comparative analysis of state-of-the-art tree-based regression algorithms.
* **Key Techniques:** Data Preprocessing, Feature Selection, **XGBoost Regression**, **LightGBM Regression**.
* **Dataset:** Red Wine variant of the Wine Quality dataset (UCI ML Repository).

### 2. Assessment 02: Wine Quality Classification

* **Business Problem:** To categorize wine into a simple 'high' or 'low' quality bracket, enabling quick decisions on batch processing or redirection for different market segments.
* **Methodology Focus:** Addressing the challenge of **class imbalance** using oversampling techniques and focusing on model transparency and trustworthiness in a classification setting.
* **Key Techniques:** **SMOTE** (Synthetic Minority Over-sampling Technique), **LIME** (Local Interpretable Model-agnostic Explanations) for interpretability, Hyperparameter Tuning.
* **Dataset:** Combined Red and White Wine Quality dataset (UCI ML Repository).

### 3. Assessment 03: Bike Share Demand Regression

* **Business Problem:** Solving the critical logistical challenge of predicting bike-share demand to optimize fleet rebalancing, thereby reducing operational costs and ensuring bike availability for customers.
* **Methodology Focus:** Advanced data transformation to normalize non-Gaussian features and dimensionality reduction to handle potential multicollinearity and improve model generalization.
* **Key Techniques:** **Yeo-Johnson Power Transformation**, **Principal Component Analysis (PCA)**, Cross-Validation, Ensemble Regression (Gradient Boosting, Extra Trees).
* **Dataset:** Bike Sharing Dataset (Daily-level data) from the UCI ML Repository.


---

## Algorithms 

### Regression Algorithms (Used in Assessments 01 & 03)
      Ridge Regression
      
      Lasso Regression
      
      ElasticNet Regression
      
      LinearSVR (Support Vector Regression)
      
      XGBoost Regressor (Extreme Gradient Boosting)
      
      LightGBM Regressor (Light Gradient Boosting Machine)
      
      Gradient Boosting Regressor
      
      Random Forest Regressor
      
      Extra Trees Regressor

### Classification Algorithms (Used in Assessment 02)
      Logistic Regression
      
      Decision Trees
      
      Random Forest Classifier
      
      XGBoost Classifier
      
      Support Vector Machines (SVC)
      
      MLP (Multi-Layer Perceptron) Classifier


---

## Setup and Installation

### Prerequisites

You need **Python 3.8+** installed on your system. Using a **virtual environment** is strongly recommended to manage dependencies.

### Environment Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YOUR_USERNAME]/predictive-analysis-using-ml-algorithms.git
    cd predictive-analysis-using-ml-algorithms
    ```

2.  **Create and Activate a Virtual Environment (Recommended):**
    ```bash
    # Create the environment
    python -m venv venv
    
    # Activate the environment
    # On macOS/Linux:
    source venv/bin/activate
    # On Windows:
    .\venv\Scripts\activate
    ```

3.  **Install Dependencies:**
    *Note: If the `requirements.txt` file is not present in the repository, create it with the packages listed below, then run the installation command.*

    ```text
    # Recommended contents of requirements.txt
    pandas
    numpy
    scikit-learn
    matplotlib
    seaborn
    plotly
    xgboost
    lightgbm
    imbalanced-learn
    lime
    missingno
    jupyterlab
    ```

    Install all required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Projects

1.  **Ensure Data is Present:** The notebooks are designed to use data files located in the **`data/`** directory. Please ensure you download the necessary files (as detailed in each respective notebook) and place them in this directory before execution.

2.  **Launch Jupyter:**
    ```bash
    jupyter lab
    # or
    jupyter notebook
    ```

3.  **Execute Analysis:** Your web browser will open to the Jupyter interface. Navigate to the root directory and open any of the `assessment_0X.ipynb` notebooks. You can run the cells sequentially to re-execute the entire data analysis, modeling, and evaluation pipeline.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for full details.

---
