# **SentinelNet-AI-Powered Network Intrusion Detection System (NIDS)**
## Project overview : 
An AI-powered Network Intrusion Detection System (NIDS) to classify network traffic as normal or malicious using machine learning. The system ingests network flow datasets, extracts features, trains classifiers, and produces alerts/logs for detected suspicious activity.
## Dataset choosen for the Project :
 CICIDS2017 Dataset : **Wednesday-workingHours.pcap_ISCX.csv**
 
#  Milestone 1  
##  What I Completed (Weeks 1 – 2)

### 1️. Dataset Acquisition & Inspection  
➤ Downloaded the **Wednesday-workingHours** dataset and other relevant capture files from the **CICIDS 2017** dataset.  
➤ Performed initial exploration using `.head()`, `.info()`, and `.describe()` to understand structure and content.  
➤ Checked **unique values**, **class distribution**, and overall dataset balance between normal and attack traffic.  
➤ Verified dataset shape and consistency across all columns.  

---

### 2️. Data Cleaning & Validation  
➤ Removed duplicates to ensure unique network-flow entries.  
➤ Handled missing values by imputing (mean / median) or removing depending on context.  
➤ Dropped irrelevant or redundant columns that added no analytical value.  
➤ Confirmed that all numeric and categorical columns were clean and valid.  

---

### 3️. Encoding Categorical Features  
➤ Converted non-numeric attributes into numerical form using:  
 ▪ **Label Encoding** – for binary or ordered categorical data.  
 ▪ **One-Hot Encoding** – for unordered categories.  
➤ Ensured encoded features were ready for ML pipelines.  
➤ Saved encoded dataset:  
 `/content/drive/MyDrive/AI Sentinet Project/Encoded_wednesday.csv`  

---

### 4️. Scaling & Normalization  
➤ Standardized all numeric features using **StandardScaler** (mean = 0, std = 1).  
➤ Ensured fair comparison of features for PCA and model training.  

---

### 5️. Train / Test Split  
➤ Used `train_test_split(..., random_state = 42)` for reproducible partitioning.  
➤ Applied **stratified sampling** to maintain class balance.  
➤ Saved separate **train** and **test** sets for later milestones.  

---

### 6️. Exploratory Data Analysis (EDA)  
➤ Generated statistical summaries and key visualizations:  
 ▪ Distribution plots and boxplots for outlier detection.  
 ▪ Correlation heatmap for feature relationships.  
➤ Saved cleaned / encoded files as:  
 ▪ `Cleaned_wednesday.csv`  
 ▪ `Encoded_wednesday.csv`  

---

#  Milestone 2  
##  What I Completed (Weeks 3 – 4)

### 1️. Feature Engineering & Dataset Preparation  
➤ Loaded the cleaned dataset from **Milestone 1**.  
➤ Split data into **features (X)** and **target (y)**.  
➤ Encoded remaining categorical variables using **LabelEncoder**.  
➤ Scaled numeric columns with **StandardScaler** to normalize variance and prepare for PCA.  

---

### 2️. Dimensionality Reduction — PCA  
➤ Applied **Principal Component Analysis (PCA)** on scaled data to reduce dimensionality.  
➤ Determined the optimal number of components via explained-variance ratio.  
➤ Visualized the first two components to observe class separation between *normal* and *attack* flows.  
➤ Saved PCA-transformed dataset for later comparison and analysis.  

---

### 3️. Feature Importance & Selection (Random Forest)  
➤ Trained a **Random Forest Classifier** on both original and PCA-transformed features.  
➤ Extracted **feature-importance scores** to rank the top predictive attributes.  
➤ Visualized importances with horizontal bar charts.  
➤ Combined Random Forest rankings with PCA insights to select the most relevant features.  

---

### 4️. Correlation & Redundancy Analysis  
➤ Computed a **correlation matrix** to identify multicollinearity among numeric variables.  
➤ Cross-checked correlation findings with PCA results to eliminate overlapping or redundant features.  
➤ Finalized a refined feature subset for supervised training.  

---

### 5️. Random Forest Model Training  
➤ Utilized the existing **train / test** split from Milestone 1 with stratified sampling.  
➤ Trained **Random Forest Classifier** with parameters:  
 ▪ `n_estimators = 50`  
 ▪ `n_jobs = -1` (for parallel processing)  
➤ Evaluated performance using **Accuracy**, **Precision**, **Recall**, and **F1-Score**.  
➤ Generated a detailed **classification report** for each class.  

---

### 6️. Feature Visualization & Refinement  
➤ Visualized top-ranked features using horizontal bar charts.  
➤ Selected top features or PCA components for retraining.  
➤ Compared refined model metrics to check for performance improvements.  
➤ Saved final **trained model** and selected features for the next milestone (unsupervised anomaly detection).  

---
