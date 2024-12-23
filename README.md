**Dengue Outbreak Prediction Using Machine Learning**

Overview

This repository contains the code, data, and analysis for our project on predicting weekly dengue case counts using environmental and meteorological data. The research leverages machine learning techniques to enhance public health interventions by providing accurate forecasts of dengue outbreaks in tropical and subtropical regions.

Key features of this project include:
	•	Utilization of climate and environmental data (e.g., temperature, humidity, precipitation, and vegetation indices) for model training.
	•	Development and evaluation of regression models for accurate prediction of dengue cases.
	•	Deployment of robust data preprocessing and feature engineering techniques.

Project Objectives

The primary objective of this research is to determine:
	•	How effectively can climatic and ecological data forecast weekly dengue cases in San Juan, Puerto Rico, and Iquitos, Peru?

Our findings aim to provide actionable insights for targeted public health strategies and resource allocation during dengue outbreaks.

Data

The dataset used in this study includes:
	•	Weekly dengue case counts for San Juan and Iquitos.
	•	Features such as temperature, precipitation, humidity, and NDVI values.
	•	Data collected between 1990 and 2010, with robust preprocessing for missing values, outliers, and feature scaling.

Machine Learning Models

Models Implemented:
	1.	Linear Regression: Used as a baseline model but exhibited limitations in capturing the dataset’s complexity.
	2.	Decision Tree: Demonstrated overfitting despite capturing non-linear interactions.
	3.	Random Forest: Achieved the best balance between training and test performance, showcasing robust generalization.
	4.	XGBoost: Performed well after hyperparameter tuning but exhibited a trade-off between variance explanation and accuracy.
	5.	Lasso Regression: Struggled with overly penalizing coefficients, leading to poor predictions.

Evaluation Metrics:
	•	Root Mean Squared Error (RMSE)
	•	Mean Absolute Error (MAE)
	•	R-Squared
	•	Adjusted R-Squared

The Random Forest model emerged as the most reliable, with high R-squared and low RMSE scores, making it suitable for deployment in public health scenarios.

Results

Key findings include:
	•	Random Forest outperformed other models with an R-squared of 0.9633 and a test RMSE of 0.5588.
	•	XGBoost, though competitive with a test RMSE of 0.5144, showed lower generalizability.
	•	Robust scaling of features significantly improved model performance by mitigating the impact of outliers.

Methodology

Data Preprocessing:
	•	Handling Missing Data: Imputation using feature means.
	•	Feature Engineering: Creation of new temporal and climate-related features.
	•	Scaling: Robust scaling to address outliers and ensure consistent model performance.

Model Optimization:
	•	Hyperparameter tuning using grid search to refine the performance of tree-based models.

Feature Importance:
	•	SHAP (SHapley Additive exPlanations) values highlighted the significance of time-related features (year, weekofyear) and climate metrics (e.g., reanalysis_air_temp_k, ndvi_nw).

 Contributors
	•	Harish Mohan
 	•	Arnaaz Khan
	•	Saanidhya Khurana

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Future Work
	•	Incorporate additional data sources, such as mobility and socioeconomic indicators, to enhance model accuracy.
	•	Explore advanced methods like deep learning for better handling of complex relationships in the data.
	•	Validate the models in real-world public health scenarios for operational improvements.
