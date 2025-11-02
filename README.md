Network Intrusion Detection System (NIDS) using Machine Learning
Project Overview

This project focuses on developing a Network Intrusion Detection System (NIDS) that leverages supervised machine learning algorithms to identify and classify network attacks. Using benchmark datasets like NSL-KDD or CICIDS2017, the system aims to detect malicious network activity and enhance cybersecurity awareness.

Milestone 1: Data Preparation
Week 1 – Project Initialization and Dataset Acquisition

Objectives:

Define project goals and expected outcomes.

Download and explore the NSL-KDD or CICIDS2017 dataset.

Understand the dataset’s structure, attributes, and attack types.

Perform basic statistical analysis and data validation.

Deliverables:

Dataset acquired and verified.

Exploratory data analysis report.

Documentation of dataset insights and statistics.

Week 2 – Data Cleaning and Preprocessing

Objectives:

Handle missing values, duplicates, and irrelevant features.

Apply encoding techniques for categorical features.

Normalize or standardize numerical columns.

Split the dataset into training and testing sets.

Deliverables:

Cleaned dataset ready for model training.

Encoded and normalized feature set.

Train-test split summary.

Milestone 2: Feature Engineering and Model Development
Week 3 – Feature Engineering and Selection

Objectives:

Analyze feature importance to determine key indicators.

Use correlation analysis or PCA for dimensionality reduction.

Create new derived features if beneficial.

Deliverables:

Finalized list of top features.

Visualization of feature relationships.

Documentation of feature selection methods.

Week 4 – Supervised Model Training

Objectives:

Train supervised ML models such as Random Forest, SVM, and Logistic Regression.

Evaluate performance using:

Accuracy

Precision

Recall

F1-score

Deliverables:

Trained model files.

Performance evaluation reports.

Comparison of model metrics.

Final Evaluation and Model Comparison

Three supervised machine learning models—Random Forest, Support Vector Machine (SVM), and Logistic Regression—were evaluated using the top 10 most significant features identified via Random Forest feature importance.

Random Forest

Accuracy: 99.81%

Delivered outstanding performance across all classes.

Demonstrated high consistency and robustness, effectively handling both majority and minority categories.

Proven to be the most reliable model for real-world network intrusion detection.

Support Vector Machine (SVM)

Accuracy: 94.46%

Captured complex nonlinear patterns effectively.

Slightly lower performance in minority classes (e.g., Class 4 and 5).

Suitable for balanced datasets with moderate complexity.

Logistic Regression

Accuracy: 91.76%

Reliable for dominant classes but less effective for minority ones.

Performs well as a baseline model or for resource-constrained environments.

Offers interpretability and simplicity.

Summary

All three models showcased strong results, validating the data preprocessing and feature engineering quality.
Among them, Random Forest outperformed the others, providing the best trade-off between accuracy, precision, and scalability—making it the most suitable choice for a production-level Network Intrusion Detection System.

Technologies Used

Language: Python

Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

Datasets: NSL-KDD / CICIDS2017




 
