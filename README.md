
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
*** Feature Engineering and Model Training***
Feature Engineering and Selection

Used a Random Forest model to find which features have the biggest impact on intrusion detection.

Performed correlation analysis and created a heatmap to identify features that were highly related to each other.

Applied PCA to reduce the number of features while keeping most of the useful information.

Chose the Top 10 most important features that help the models detect attacks more accurately.

Saved this cleaned and reduced dataset for later training and model evaluation.

Week 4: Model Training and Evaluation

Scaled all selected features so that the models receive uniform input values.

Divided the dataset into 80% training and 20% testing for fair model evaluation.

Trained and tested three different machine learning models:

Random Forest Classifier – reached 98.75% accuracy

Support Vector Machine (SVM) – reached 87.51% accuracy

Logistic Regression – reached 86.69% accuracy

Compared model results by checking accuracy, precision, recall, and F1-score to see which model performed best

#### **Milestone 3:**
**Anomaly Detection and Model Evaluation**


Week 5: Anomaly Detection using Unsupervised Learning

Used unsupervised models like K-Means and Isolation Forest to find unusual patterns in network traffic.

Identified abnormal behavior that differs from normal activity, simulating zero-day attacks.

Created visual plots to show how normal and suspicious traffic are grouped.

Checked the accuracy of anomaly detection by comparing results with the true labels in the test dataset.

Week 6: Model Evaluation and Fine-Tuning

Evaluated multiple models such as Random Forest, SVM, and Isolation Forest.

Applied cross-validation to adjust model parameters and improve accuracy.

Generated confusion matrices and ROC curves to visually compare model performance.

Chose the best model based on F1-score and recall, which measure detection quality.

Recorded all results and performance metrics for final reporting.
