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
    
    - Applied Principal Component Analysis (PCA) for dimensionality reduction while retaining 90% variance.  
    
    - Trained a Random Forest model to identify Top 10 most important features contributing to attack detection.
    
    - Extracted and visualized the Top 10 most important features influencing attack detection using Random Forest.

2. Supervised Model Training

    - Trained and compared three models using only the Top 10 selected features:

       - Random Forest Classifier (n_estimators = 50)  

       - Support Vector Machine (SVM) with RBF kernel  

       - Logistic Regression (max_iter = 1000)  

4. Model Evaluation
    
    - Random Forest: Achieved 99.20% accuracy, best overall performance with near-perfect precision, recall, and F1-score.  
    
    - Logistic Regression: Achieved 94.33% accuracy.
    
    - SVM: Achieved 95.80% accuracy, good for nonlinear patterns, slightly lower recall for rare attacks.

5. Key insights
    
    - PCA reduced data dimensions significantly while maintaining accuracy.  
    
    - Random Forest identified critical attack-related features(top 10 features).  
    
    - All models achieved above 94% accuracy, proving strong dataset quality and effective preprocessing.
      
## Milestone 3: Anomaly Detection with Unsupervised Learning

1. K-Means Clustering

    - Applied K-Means (n_clusters=2) for normal vs. abnormal traffic.

    - Detected 1.74% anomalies based on distance from cluster centroids.

    - Effective for clear separations but less sensitive to subtle variations.

2. Isolation Forest

    - Applied Isolation Forest (n_estimators=100, contamination='auto').

    - Detected ~20.78% anomalies, showing higher sensitivity to rare and hidden attack patterns.

    - More effective for identifying complex and subtle network anomalies.

3. Conclusion
   Unsupervised anomaly detection was performed using the top 10 selected features. K-Means detected 1.74% anomalies, while Isolation Forest identified 20.78%. K-Means was efficient but missed subtle variations. Isolation Forest isolated complex, rare anomalies more effectively.
   
## Tech Stack

- **Language:** Python  

- **Libraries:** pandas, numpy, seaborn, matplotlib, scikit-learn  

- **Dataset:** CICIDS 2017 - Wednesday Working Hours subset  

- **Environment:** Google Colab

## Dataset Access

The datasets used in this project are derived from the CICIDS 2017 - Wednesday Working Hours subset, which contains both normal and attack network traffic records.

Due to large file sizes, the datasets cannot be uploaded to GitHub. They are securely stored and can be accessed using the following Google Drive link:

**Dataset Drive Link:** [Data]([https://drive.google.com/your-drive-link-here](https://drive.google.com/drive/folders/1foF7ZF19cuIG8njbmZSc-9Yz61q7f3MH?usp=sharing))

Files Included:

Wednesday.csv - Original dataset extracted from the CICIDS 2017 collection. Used as the raw source for preprocessing.

cleaned_data.csv - Cleaned and filtered dataset after removing missing values, duplicates, and irrelevant columns. Used as the base for further transformation.

sentinelnet_encoded.csv - Encoded and standardized dataset where categorical labels were converted using LabelEncoder. Used as the main dataset for both supervised and unsupervised model training.

Dataset Source:
Official CICIDS 2017 Dataset - https://www.unb.ca/cic/datasets/ids-2017.html

