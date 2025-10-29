SentinelNet: AI-Powered Network Intrusion Detection System (NIDS)

SentinelNet is an intelligent Network Intrusion Detection System (NIDS) powered by machine learning.
It analyzes network traffic patterns to detect malicious activities, leveraging advanced feature engineering and AI-driven classification models to identify potential threats in real-time.

Project Goals

Develop an AI-powered NIDS to detect malicious network traffic.

Understand and analyze network traffic patterns and attack behaviors.

Apply machine learning models for accurate intrusion detection.

Perform feature engineering to extract key characteristics from data.

Generate alerts and analytical reports for suspicious network activities.

Dataset: CICIDS2017 – Wednesday Subset

Source: Canadian Institute for Cybersecurity (CIC)

The dataset includes both benign and malicious network traffic records with various attack types such as DDoS, PortScan, Brute Force, and more.

📊 Data Exploration

Explored dataset structure, feature types, and unique attack labels.

Performed statistical analysis and distribution validation.

Visualized missing values, categorical features, and class imbalance.


Data Cleaning

Identified and visualized missing values using heatmaps.

Dropped null and duplicate rows.

Removed irrelevant features and standardized column naming.

Validated cleaned data for integrity and completeness.


Data Preprocessing

Encoding: Categorical Label column encoded with LabelEncoder.

Scaling: Numerical features standardized (mean ≈ 0, std ≈ 1).

Visualization: Compared feature distributions before and after scaling.

Splitting: Dataset divided into Training (80%) and Testing (20%) subsets.

Feature Engineering & Selection

Conducted feature importance analysis using Random Forest.

Visualized correlation heatmap to detect multicollinearity.

Applied Principal Component Analysis (PCA) for dimensionality reduction.

Selected Top 10 important features contributing most to intrusion detection.

Saved refined dataset for efficient model training and evaluation.

