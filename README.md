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

       - Support Vector Machine (SVM)

       - Logistic Regression (max_iter = 1000)  

4. Model Evaluation
    
    - Random Forest: Achieved 99.57% accuracy, best overall performance with near-perfect precision, recall, and F1-score.  
    
    - Logistic Regression: Achieved 87.95% accuracy.
    
    - SVM: Achieved 84.80% accuracy.

5. Key insights
    
    - PCA reduced data dimensions significantly while maintaining accuracy.  
    
    - Random Forest identified critical attack-related features(top 10 features).  
    
    - All models successfully learned attack patterns, with Random Forest being the best performer.
      
## Milestone 3: Anomaly Detection with Unsupervised Learning

1. K-Means Clustering

    - Applied K-Means clustering using the optimal number of clusters (k = 5) determined through the Elbow Method and Silhouette Score to group different traffic behavior patterns and identify anomalies.

    - Detected 1.02% anomalies based on distance from cluster centroids.

    - Useful for simple cluster-based separation but less sensitive to subtle anomalies.

2. Isolation Forest

    - Applied Isolation Forest (contamination = 0.01, default n_estimators = 100) on the scaled test data to identify outliers and detect anomalous traffic patterns.

    - Detected 0.91% anomalies.

    - Better at identifying complex and rare attack patterns compared to K-Means.

3. Supervised Model comparison - Compared supervised models (Random Forest, SVM, Logistic Regression).

4. Hyperparameter Tuning
    - Performed hyperparameter tuning using GridSearchCV / RandomizedSearchCV with cross-validation on the training set to find optimal model parameters.

    - For the Random Forest, tuned parameters included n_estimators, max_depth, min_samples_split, min_samples_leaf, and criterion. Example final tuned parameters used in the project: n_estimators=50, min_samples_split=5, min_samples_leaf=2, criterion='entropy', random_state=42.

    - For SVM and Logistic Regression, tuned parameters such as C, kernel (SVM), and max_iter (Logistic Regression) were considered.
    - After tuning and validating with cross-validation, model performance on cross-validation folds and final test set were reported. The Random Forest remained the best model overall.

5. Conclusion
     Unsupervised anomaly detection was performed using the Top 10 selected features. K-Means detected 1.02% anomalies, whereas Isolation Forest detected 0.91%. Isolation Forest proved more effective at isolating subtle and hidden intrusion.
   Systematically compared models and tuned hyperparameters with cross-validation; Random Forest was selected as final supervised model due to its highest cross-validated performance and stability on the test set.

## Milestone 4: Alert Generation & Logging
- A hybrid alert engine was implemented:
    If (RandomForest predicts attack) OR (IsolationForest flags anomaly):
        Final Alert = "ALERT"
    Else:
        Final Alert = "NORMAL"

- Generated log file: SentinelNet_NIDS_Alert_Log.csv
        This file includes: Final Alert, RF Predicted Label, IF Anomaly Flag, True Label, Selected features
- This log is used by the Streamlit Dashboard.

## Tech Stack

- **Language:** Python  

- **Libraries:** pandas, numpy, seaborn, matplotlib, scikit-learn  

- **Dataset:** CICIDS 2017 - Wednesday Working Hours subset  

- **Environment:** Google Colab
  
- **Dashboard:** Streamlit

## Dataset Access

The datasets used in this project are derived from the CICIDS 2017 - Wednesday Working Hours subset, which contains both normal and attack network traffic records.

Due to large file sizes, the datasets cannot be uploaded to GitHub. They are securely stored and can be accessed using the following Google Drive link:

**Dataset Drive Link:** [Data](https://drive.google.com/drive/folders/1foF7ZF19cuIG8njbmZSc-9Yz61q7f3MH?usp=sharing)

Files Included:

Wednesday.csv - Original dataset extracted from the CICIDS 2017 collection. Used as the raw source for preprocessing.

cleaned_data.csv - Cleaned and filtered dataset after removing missing values, duplicates, and irrelevant columns. Used as the base for further transformation.

sentinelnet_encoded.csv - Encoded and standardized dataset where categorical labels were converted using LabelEncoder. Used as the main dataset for both supervised and unsupervised model training.

Dataset Source:
Official CICIDS 2017 Dataset - https://www.unb.ca/cic/datasets/ids-2017.html

