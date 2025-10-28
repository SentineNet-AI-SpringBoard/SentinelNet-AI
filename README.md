# SentinelNet-AI-Powered Network Intrusion Detection System (NIDS) 

### Overview
**SentinelNet-AI** is an AI-powered Network Intrusion Detection System developed to detect malicious network traffic using machine learning techniques.  
This project uses the **CICIDS 2017 Wednesday dataset**.

## Milestone 1: Project Initialization, Dataset Acquisition, and Preprocessing

1. Project Goals and Expected Outcomes

    -Develop an AI-based NIDS to detect malicious network activity.

    -Understand network traffic data and attack types.

    -Apply machine learning models for intrusion detection.

    -Perform feature engineering and identify the most important features.

    -Generate alerts for suspicious activity and prepare analytical reports.

2. Dataset Acquisition and Exploration

    -Dataset: CICIDS2017 (Wednesday subset) from CIC Dataset.

    -Explored dataset structure, feature types, and unique attack labels.

    -Performed basic statistics and data validation to understand feature distributions.

    -Visualized data to detect anomalies and ensure data quality.

3. Data Cleaning

    -Identified missing values and visualized them using heatmaps.

    -Dropped rows with null values and removed duplicate entries.

    -Removed irrelevant features and cleaned column names for consistency.

4. Data Preprocessing

    -Encoded the categorical target column Label using LabelEncoder.

    -Standardized numerical features using StandardScaler.
   
    -Visualized feature distributions.

6. Dataset Splitting

    -Split the dataset into training (70%) and testing (30%) subsets.

    -Prepared datasets for machine learning model development and evaluation.

## Milestone 2: Feature Engineering, Supervised Model Training, and Evaluation

1. Feature Engineering
   
    - Performed correlation analysis to identify highly correlated features.
    
    - Applied Principal Component Analysis (PCA) for dimensionality reduction while retaining 95.6% variance.  
    
    - Scaled and transformed the dataset to enhance model learning efficiency.  
    
    - Extracted and visualized the Top 10 most important features influencing attack detection using Random Forest.

2. Supervised Model Training
    - Trained and compared three supervised models:

       - Random Forest Classifier (n_estimators = 50)  

       - Support Vector Machine (SVM) with RBF kernel  

      - Logistic Regression with max_iter = 1000  

3. Model Evaluation
    
    - Random Forest: Achieved 99.92% accuracy, best overall performance with near-perfect precision, recall, and F1-score.  
    
    - Logistic Regression: Achieved 99.21% accuracy, efficient and stable across most classes.  
    
    - SVM: Achieved 98.93% accuracy, strong nonlinear modeling with slightly lower recall on rare attacks.

4. Key insights
    
    - PCA reduced data dimensions significantly while maintaining accuracy.  
    
    - Random Forest identified critical attack-related features.  
    
    - All models achieved accuracy above 98%, confirming high data quality and robust preprocessing.

## Tech Stack

- **Language:** Python  

- **Libraries:** pandas, numpy, seaborn, matplotlib, scikit-learn  

- **Dataset:** CICIDS 2017 - Wednesday Working Hours subset  

- **Environment:** Google Colab  

