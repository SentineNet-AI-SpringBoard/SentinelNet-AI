# **SentinelNet-AI-Powered Network Intrusion Detection System (NIDS)**
## Project overview : 
An AI-powered Network Intrusion Detection System (NIDS) to classify network traffic as normal or malicious using machine learning. The system ingests network flow datasets, extracts features, trains classifiers, and produces alerts/logs for detected suspicious activity.
## Dataset choosen for the Project :
 CICIDS2017 Dataset : **Wednesday-workingHours.pcap_ISCX.csv**
# Milestone 1
## What I completed (Weeks 1–2) 
### 1. Dataset acquisition & inspection
* Downloaded the Wednesday dataset and other relevant captures.
* Performed initial exploration (head, unique values, class balance, basic counts).
### 2. Data cleaning & validation
* Removed duplicates.
* Handled missing values (identified columns with gaps and either imputed or removed depending on context).
* Removed irrelevant or redundant columns.
### 3. Encoding categorical features
* Converted all categorical columns to numeric form (Label Encoding / One-Hot where applicable).
* Saved encoded version as /content/drive/MyDrive/AI Sentinet Project/Encoded_wednesday.csv.
### 4. Scaling & normalization
* Standardized numeric features to zero mean and unit variance (required for PCA and for ensuring fair feature importance comparisons).
### 5. Train/test split
* Created reproducible splits (e.g., train_test_split(..., random_state=42)), saving separate train/test sets where appropriate.
### 6. Exploratory analysis artifacts
* Visualizations: distribution plots, boxplots for outlier checks, correlation heatmap
* Basic statistics (mean, std, min, max) and data types summary.
All cleaned/encoded files are saved in my Drive paths (Cleaned_wednesday.csv and Encoded_wednesday.csv).
## Quick concept explanations
### Data acquisition & structure
* Network flow datasets (rows = flows / sessions). Typical fields: timestamps, bytes/packets counts, durations, protocol/ports, and derived flow statistics.
* Understanding attack labels and categories early helps sampling and labeling logic.
### Missing values & duplicates
* Missing values: can bias models. Options: drop rows/columns, impute (median/mean for numeric), or flag with indicator columns.
* Duplicates: removed to avoid over-counting identical flows.
### Encoding categorical data
* **Label encoding :** maps categories to integers (fast, but ordinal meaning may be implicit).
* **One-hot encoding :** creates binary columns for categories (useful when categories are unordered).
* Use encoded dataset for all subsequent ML steps.
### Feature scaling
* Scaling (StandardScaler) is important for PCA and distance-based models. It centers features and scales variance to 1.
### PCA (why & when)
* Principal Component Analysis reduces dimensionality by projecting features onto orthogonal axes that explain the greatest variance.
* Use PCA to identify redundancy and for visualization; do not use PCA-transformed features for interpreting original feature importances (they’re combinations of original features).
### Train/test split
* Splitting ensures evaluation on unseen data. Typical split: 80% train / 20% test. Use random_state for reproducibility.
## Files Included : 
* **"SentinelNet.ipynb" :** Main Colab notebook containing all code and analysis.
* **"Cleaned_wednesday.csv":** cleaned (missing values handled, duplicates removed).
* **"Encoded_wednesday.csv" :** cleaned + categorical features encoded (this is the working file used for PCA/RF).
* **"CleanedData/Wednesday_top10_features.csv" :** subset containing top 10 RF features + label.
## Tools & Environments Used :
* Google Colab (drive mount for I/O)
* Python 3.x
* Pandas / NumPy (data handling)
* Scikit-learn (StandardScaler, PCA, RandomForestClassifier, train_test_split)
* Matplotlib / Seaborn (visualizations)
* Git & GitHub (version control & branch management)
