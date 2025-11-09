# assignment-8-Jerlinchellam12

Name : Jerlin Chellam J

Roll No: DA25C009

Documentation


# Ensemble Learning for Complex Regression — Bike Share Demand Prediction  

## Introduction  
This project focuses on predicting the total count of rented bikes in a city’s bike-sharing system using **ensemble learning techniques**. Accurate forecasting helps the city manage inventory and resources effectively. Since bike demand depends on many factors like weather, season, and time, this becomes a **complex regression problem** with non-linear relationships.  

## Overview  
I explored three primary ensemble techniques - **Bagging**, **Boosting**, and **Stacking** — to handle the challenges of high variance and bias in predictive modeling.  

Each method was implemented and compared based on its performance in predicting bike demand, measured using the **Root Mean Squared Error (RMSE)** metric.  

## Objectives  
- To apply and understand different ensemble learning methods for regression.
  
- To compare single models and ensemble models in terms of RMSE and generalization.
  
- To analyze how ensemble methods reduce bias and variance.
  
- To identify the most effective ensemble approach for the Bike Sharing dataset.  

## Requirements  
- **Language:** Python
  
- **Libraries Used:**  
  - pandas  
  - numpy  
  - scikit-learn  
  - matplotlib  
  - seaborn  
  - jupyter notebook  

Ensure all dependencies are installed before running the notebook.  

## 📊 Dataset and Methodology  
- **Dataset:** [Bike Sharing Dataset (Hourly)](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset)  
- **Source:** UCI Machine Learning Repository  
- **Size:** 17,379 hourly records  

### Methodology Steps  
1. **Data Preprocessing:**  
   - Loaded and cleaned data.  
   - Dropped irrelevant columns (`instant`, `dteday`, `casual`, `registered`).  
   - Encoded categorical features using One-Hot Encoding.  

2. **Baseline Models:**  
   - Trained **Decision Tree Regressor** and **Linear Regression**.  
   - Selected the better model (Linear Regression, RMSE: 100.44) as the baseline.  

3. **Ensemble Techniques:**  
   - **Bagging Regressor:** Reduced variance (RMSE: 112.11).  
   - **Gradient Boosting Regressor:** Reduced bias effectively (RMSE: 80.59).  
   - **Stacking Regressor:** Combined multiple models (RMSE: 62.48).  

4. **Evaluation Metric:**  
   - Root Mean Squared Error (RMSE) was used to compare model performance.  

## 🔍 Observations  
- Linear Regression handled linear relationships well but missed complex patterns.
   
- Bagging stabilized predictions and reduced overfitting from Decision Trees.
  
- Boosting corrected errors sequentially and captured complex non-linear relations.
    
- Stacking combined diverse model strengths and achieved the **best overall performance** with the lowest RMSE (62.48).  

## ✅ Conclusion  
The **Stacking Regressor** emerged as the best-performing model, effectively combining the predictive strengths of KNN, Bagging, and Gradient Boosting through a Ridge Regression meta-learner. 

This project showed how ensemble methods can significantly improve predictive performance by balancing **bias** and **variance**.  

It reinforced the idea that model diversity and smart combination strategies can outperform even the best single model.  

## 📚 Reference  
- *Bike Sharing Dataset*. UCI Machine Learning Repository.
  
- Scikit-learn Documentation: [https://scikit-learn.org/](https://scikit-learn.org/)  
