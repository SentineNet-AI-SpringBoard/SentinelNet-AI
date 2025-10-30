# SentinelNet: AI-Powered Network Intrusion Detection System (NIDS)

## Milestone 1: Project Initialization, Dataset Acquisition, and Preprocessing

### 1. Project Goals and Expected Outcomes
- Develop an AI-powered NIDS to detect malicious network traffic.
- Understand network traffic data and attack types.
- Apply ML models to detect intrusions.
- Perform feature engineering and select important features.
- Generate alerts for suspicious activity and prepare a report.

### 2. Dataset Acquisition and Exploration
- Dataset: CICIDS2017 (Wednesday subset) from [CIC Dataset](https://www.unb.ca/cic/datasets/ids-2017.html).
- Explored dataset structure, feature types, and unique attack labels.
- Performed basic statistics and data validation to understand data distribution.

### 3. Data Cleaning
- Identified and visualized missing values using heatmaps.
- Dropped rows with null values and duplicate rows.
- Removed irrelevant features and cleaned column names.

### 4. Data Preprocessing
- Encoded categorical target column `Label` using `LabelEncoder`.
- Standardized numerical features (mean ~0, std ~1) for uniform scaling.
- Visualized distributions of numerical features before and after scaling.

### 5. Dataset Splitting
- Split dataset into training (80%) and testing (20%) sets for ML model development.
  
## Milestone 2: Feature Engineering and Model Training

### 1. Feature Engineering and Selection
- Analyzed feature importance using **Random Forest** to identify significant features influencing intrusion detection.  
- Conducted **correlation analysis** and visualized a heatmap to detect multicollinearity among variables.  
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction while retaining most of the data variance.  
- Selected **Top 10 important features** contributing most to the prediction of attacks.  
- Saved the refined dataset for model training and evaluation.  

### 2. Model Training and Evaluation
- Standardized the selected features to ensure consistent scaling for all models.  
- Split the dataset into **training (80%)** and **testing (20%)** subsets.  
- Trained and evaluated the following **machine learning models**:  
  - **Random Forest Classifier** – Achieved **99.20% accuracy**  
  - **Support Vector Machine (SVM)** – Achieved **95.91% accuracy**  
  - **Logistic Regression** – Achieved **94.69% accuracy**  
- Compared all models using **accuracy**, **precision**, **recall**, and **F1-score** metrics.  
