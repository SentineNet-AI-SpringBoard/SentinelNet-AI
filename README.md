
# **SentinelNet: AI-Powered Network Intrusion Detection System (NIDS)**

## **Milestone 1: Project Initialization, Dataset Acquisition, and Preprocessing**

### **1. Project Goals and Expected Outcomes**

* The main goal of this project is to build an **AI-based Network Intrusion Detection System (NIDS)** that can identify and alert users about **malicious or suspicious network traffic**.
* Understand how network traffic works and learn about different **attack types** (e.g., DoS, DDoS, Port Scan, etc.).
* Use **machine learning algorithms** to automatically detect these attacks.
* Perform **feature selection and feature engineering** to improve model performance.
* Create a simple alert system that warns about intrusions and generates a **detailed report** of the detected activities.

---

### **2. Dataset Acquisition and Exploration**

* The dataset used is **CICIDS2017 (Wednesday subset)**, downloaded from the [CIC Dataset Repository](https://www.unb.ca/cic/datasets/ids-2017.html).
* This dataset contains both **normal** and **malicious** network traffic samples.
* The dataset includes various network features like **packet length, flow duration, source/destination ports, and flag counts**.
* During exploration:

  * We checked the **structure** of the dataset (number of rows, columns, and data types).
  * Analyzed **unique attack labels** to understand which types of intrusions are present.
  * Calculated **basic statistics** (mean, median, min, max) for each feature to identify data ranges and potential outliers.

---

### **3. Data Cleaning**

* Checked for **missing values** and visualized them using a **heatmap** for better understanding.
* Removed all **rows with missing or invalid values** to ensure data quality.
* Dropped **duplicate records** that could bias the model.
* Removed **irrelevant features** such as timestamps, IP addresses, and other identifiers that do not help in training.
* Renamed columns to clean, consistent names for easier processing.

---

### **4. Data Preprocessing**

* Used **Label Encoding** on the target column `Label` to convert attack types (text) into numeric form for machine learning.
* Applied **feature scaling (standardization)** so that all numerical features have a similar range — this helps the model train more effectively.
* Visualized **data distributions before and after scaling** using histograms to confirm that scaling worked properly.
* Verified that all features are in suitable formats (numerical values only) for model training.

---

### **5. Dataset Splitting**

* The cleaned and processed dataset was split into two parts:

  * **Training set (80%)** – used to train the machine learning models.
  * **Testing set (20%)** – used to evaluate model performance on unseen data.
* Ensured both subsets have a **balanced distribution** of attack and normal traffic records.
* Saved the final preprocessed datasets for use in the **next milestones**, where different ML models (like Random Forest and SVM) will be trained and compared.
### **Milestone 2:**
*  Feature Engineering, Supervised Model Training, and Evaluation
Feature Engineering

Conducted correlation analysis to remove redundant and highly correlated features.

Applied Principal Component Analysis (PCA) to reduce feature dimensions while retaining 90% of the data’s variance.

Trained a Random Forest model to determine the Top 10 most informative features for attack classification.

Extracted and visualized these Top 10 features to understand their importance in detecting attacks.

Supervised Model Training

Three machine learning models were trained using only the Top 10 selected features:

Random Forest Classifier with 50 trees

Support Vector Machine (SVM) with RBF kernel

Logistic Regression with 1000 max iterations

Model Evaluation

Random Forest achieved 99.20% accuracy with strong precision, recall, and F1-score.

SVM achieved 95.80% accuracy with good performance on nonlinear data.

Logistic Regression achieved 94.33% accuracy and served as a strong baseline model.

Key Insights

PCA effectively reduced data complexity without significant loss of accuracy.

Random Forest identified the most relevant attack-related features.

All models achieved over 94% accuracy, reflecting solid dataset quality and preprocessing steps.
### ***Milestone 3:**
 Anomaly Detection with Unsupervised Learning
K-Means Clustering

Applied K-Means with 2 clusters to classify data as normal or abnormal.

Detected around 1.74% anomalies based on distances from cluster centers.

Performed well for distinct patterns but was less sensitive to minor anomalies.

Isolation Forest

Used Isolation Forest with 100 decision trees and automatic contamination detection.

Detected approximately 20.78% anomalies, demonstrating higher sensitivity to rare and subtle patterns.

Better suited for complex and varied network anomalies.
