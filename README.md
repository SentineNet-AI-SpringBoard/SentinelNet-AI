# SentinelNet-AI-Powered Network Intrusion Detection System (NIDS)

### Overview
**SentinelNet-AI** is an AI-powered Network Intrusion Detection System developed to detect malicious network traffic using machine learning techniques.
This project uses the **CICIDS 2017 Wednesday dataset**.

## Milestone 1: Project Initialization, Dataset Acquisition, and Preprocessing

1. Project Goals and Expected Outcomes

    -Develop an AI-powered NIDS to detect malicious network traffic.
   
    -Understand network traffic data and attack types.

    -Apply ML models to detect intrusions.

    -Perform feature engineering and select important features.

    -Generate alerts for suspicious activity and prepare a report.

3. Dataset Acquisition and Exploration

    -Dataset: CICIDS2017 (Wednesday subset) from CIC Dataset.

    -Explored dataset structure, feature types, and unique attack labels.

    -Performed basic statistics and data validation to understand data distribution.

4. Data Cleaning

    -Identified and visualized missing values using heatmaps.

    -Dropped rows with null values and duplicate rows.

    -Removed irrelevant features and cleaned column names.

5. Data Preprocessing 

    -Encoded categorical target column Label using LabelEncoder.

    -Standardized numerical features (mean ~0, std ~1) for uniform scaling.

    -Visualized distributions of numerical features before and after scaling.

6. Dataset Splitting

    -Split dataset into training (80%) and testing (20%) sets for ML model development.
