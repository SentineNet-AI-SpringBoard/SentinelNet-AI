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
