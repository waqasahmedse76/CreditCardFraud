This project  highlights credit card fraud by training Machine Learning models on data sourced from Kaggle. The Kaggle Credit Card Fraud Detection dataset is utilized, which contains highly imbalanced classes with only 0.17% fraudulent transactions.

Methodology
The dataset was preprocessed by standardizing the numerical features using StandardScaler. Given the class imbalance, Synthetic Minority Over-sampling Technique (SMOTE) was employed to balance the dataset before training supervised models. The dataset was split into training and validation sets (80%-20%).

Three models were selected for evaluation:
•	Logistic Regression (Supervised)
•	XGBoost Classifier (Supervised)
•	Isolation Forest (Unsupervised)

The supervised models were trained using the balanced dataset, whereas the Isolation Forest model was trained on the original dataset under the assumption that anomalies (fraud cases) are rare and should be distinguishable from normal transactions.

Model Performance and Selection

Each model was evaluated using Accuracy, Precision, Recall, F1-Score, and AUC-ROC scores. The results indicated the following:

•	XGBoost achieved the highest performance with a strong AUC-ROC score, demonstrating its ability to capture fraudulent patterns effectively.

•	Logistic Regression performed well but showed lower recall compared to XGBoost, indicating a slightly higher rate of missed fraud cases.

•	Isolation Forest, as an unsupervised approach, struggled with precision and recall, demonstrating the challenges of detecting fraud without labeled data.
 
Improvements Made
There were several improvements made to the project. StandardScaler was introduced to improve model convergence, and redundant features were excluded. Furthermore, SMOTE helped in improving recall for supervised models by addressing class imbalance. Lastly ROC Curvy Analysis helped in the evaluation of model thresholds to reduce false positives while maintaining high recall.
