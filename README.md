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

### Week - 5: Feature Engineering and Selection
- Analyzed feature importance using **Random Forest** to identify significant features influencing intrusion detection.  
- Conducted **correlation analysis** and visualized a heatmap to detect multicollinearity among variables.  
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction while retaining most of the data variance.  
- Selected **Top 10 important features** contributing most to the prediction of attacks.  
- Saved the refined dataset for model training and evaluation.  

### Week - 4: Model Training and Evaluation
- Standardized the selected features to ensure consistent scaling for all models.  
- Split the dataset into **training (80%)** and **testing (20%)** subsets.  
- Trained and evaluated the following **machine learning models**:  
  - **Random Forest Classifier** – Achieved **99.20% accuracy**  
  - **Support Vector Machine (SVM)** – Achieved **95.91% accuracy**  
  - **Logistic Regression** – Achieved **94.69% accuracy**  
- Compared all models using **accuracy**, **precision**, **recall**, and **F1-score** metrics.

## 📍 Milestone 3: Anomaly Detection and Model Evaluation

### Week 5: Anomaly Detection using Unsupervised Learning
- Implemented unsupervised algorithms such as **K-Means** and **Isolation Forest** to identify unusual network traffic patterns.  
- Detected anomalies deviating from normal behavior to simulate zero-day attacks.  
- Visualized clustering results to understand the separation between normal and suspicious traffic.  
- Evaluated anomaly detection capability by comparing with labeled data from the test set.

### Week 6: Model Evaluation and Fine-tuning
- Compared multiple models including **Random Forest, SVM, and Isolation Forest**.  
- Used **cross-validation** for hyperparameter tuning to improve detection accuracy.  
- Generated **confusion matrix** and **ROC curves** for visual performance comparison.  
- Selected the best-performing model based on **F1-score** and **recall** metrics.  
- Documented results and model performance statistics for reporting.

---

## 📍 Milestone 4: Alert Generation and Logging

### Week 7: Real-time Alert Generation and Logging
- Simulated real-time intrusion detection using test data.  
- Generated alerts for identified intrusions and categorized them by severity level.  
- Implemented logging to store all alerts and detections in a **CSV file** using:
