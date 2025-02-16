Failure Classification in MetroPT 3 Dataset: Final Report
1. Introduction
1.1 Project Overview
The primary objective of this project was to develop a machine learning model to classify and predict failures in the MetroPT 3 dataset. By analyzing various sensor readings and operational parameters, we aimed to build a robust failure detection system that can assist in predictive maintenance.
1.2 Problem Statement
Unplanned system failures can result in operational inefficiencies and increased maintenance costs. Therefore, accurately predicting failures using sensor data can help in proactive maintenance, reducing downtime and improving efficiency.
2. Dataset Overview
2.1 Data Description
The dataset consists of multiple features related to system operations, including:
•	Sensor Readings: DV_pressure, TP2, TP3, Oil_temperature, etc.
•	Operational Parameters: Motor_current, COMP, Reservoirs, etc.
•	Target Variable: Failure (Binary: 0 for No Failure, 1 for Failure)
2.2 Data Preprocessing
•	Converted timestamps to datetime format.
•	Handled missing values.
•	Standardized feature scaling.
•	Balanced the dataset using resampling techniques where necessary.
3. Model Selection and Evaluation
3.1 Machine Learning Models Used
We evaluated the following models:
1.	Logistic Regression
2.	Decision Tree Classifier
3.	Random Forest Classifier
4.	XGBoost Classifier
3.2 Performance Metrics
•	Accuracy: Measures overall correctness of the model.
•	Precision: Fraction of correctly predicted failures among all predicted failures.
•	Recall: Fraction of actual failures correctly identified.
•	F1-Score: Harmonic mean of precision and recall.
3.3 Model Comparison
Model	Accuracy	Precision (Class 1)	Recall (Class 1)	F1-Score (Class 1)
Logistic Regression	0.99	0.75	0.80	0.77
Decision Tree	1.00	0.98	0.98	0.98
Random Forest	1.00	0.98	0.99	0.99
XGBoost	1.00	0.98	0.98	0.98
4. Final Model Selection: Random Forest
4.1 Justification
•	Best Recall (0.99 for Class 1 - Failures): Ensures that almost all failures are detected.
•	High Precision & F1-Score (0.98 & 0.99): Maintains low false positives while ensuring reliable classification.
•	Feature Importance Insights: Allows interpretability for understanding key failure predictors.
•	Generalization & Robustness: Handles complex data patterns and is less prone to overfitting compared to a single decision tree.
4.2 Feature Importance Analysis
A feature importance comparison between XGBoost and Random Forest showed that:
•	DV_pressure, TP3, and Oil_temperature are the most critical factors in failure prediction.
•	Reservoirs and LPS also play a significant role.
5. Conclusion and Future Work
5.1 Key Takeaways
•	The Random Forest model is the best choice for failure classification due to its high performance.
•	Feature importance analysis helps in understanding the most relevant factors for failures.
•	The model can be integrated into real-time failure prediction systems to assist in predictive maintenance.
5.2 Future Work
•	Deploy the model in a real-time monitoring system.
•	Optimize the model further with hyperparameter tuning.
•	Explore deep learning approaches for even better predictive accuracy.
6. References
•	Dataset source (if applicable)
•	Machine Learning libraries used: Scikit-Learn, XGBoost, Pandas, Matplotlib
•	Research papers/articles related to failure classification
Dataset Link ;-https://drive.google.com/drive/folders/1bli9ylBYXaLqDUhHNZdFYv0IfUuw1aXX?usp=sharing
________________________________________
Prepared by: SANJAY S
