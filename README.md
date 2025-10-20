# SentinelNet-AI-Powered Network Intrusion Detection System (NIDS) 

### Overview
**SentinelNet-AI** is an AI-powered Network Intrusion Detection System developed to detect malicious network traffic using machine learning techniques.  
This project uses the **CICIDS 2017 Wednesday dataset** and implements data preprocessing, feature engineering, PCA, and Random Forest–based feature importance extraction.

## Project Structure

1. Dataset Acquisition & Exploration

    -Loaded the dataset and inspected its structure.

    -Checked data types and summary statistics.

2. Data Cleaning & Preprocessing

    -Handled missing values.

    -Removed irrelevant columns.

    -Detected outliers.

    -Encoded categorical labels.

3. Feature Engineering & Selection

    -Applied feature scaling.

    -Performed PCA retaining 95% variance.

    -Extracted top 10 important features using Random Forest.

## Technical Workflow
1. Data Cleaning and Encoding  
2. Outlier Detection using IQR  
3. Feature Scaling (StandardScaler)  
4. Dimensionality Reduction using PCA  
5. Top 10 Feature Extraction (Random Forest, n_estimators=50)  
6. Train-Test Split (70–30)


## Files included

- **'SentinelNet-AI.ipynb'** – Main Colab notebook containing all code and analysis.
- **'sentinelnet_encoded.csv'** – Cleaned and encoded dataset.
- **'sentinelnet_pca.csv'** – PCA-transformed dataset.
- **'top10_features.csv'** – Extracted top 10 important features.
- **'.gitignore'** – Excludes raw datasets and temporary files from version control.


## Tools Used
- Python, Pandas, NumPy, Matplotlib, Seaborn  
- Scikit-learn (StandardScaler, PCA, RandomForestClassifier)  
- Google Colab
