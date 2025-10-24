# **SentinelNet-AI-Powered Network Intrusion Detection System (NIDS)**

The Dataset used in this project is CICIDS2017, obtained from the official source of the Canadian Institute for Cybersecurity.
Dataset:https://www.unb.ca/cic/datasets/ids-2017.html

Milestone_1.ipynb contains the code of week 1 and week 2

## **Week-1 Project Initializaon and Dataset Acquision**

This initial phase is all about setting the stage for the project. We'll define our objectives, get the necessary data, and perform a first-pass analysis to understand what we're working with.

**1.Define project goals and expected outcomes.**

**Project Goal:** The primary goal is to develop and evaluate a machine learning model for Network Intrusion Detection. This system will be trained to distinguish between normal network traffic and malicious activities ("attacks").

**Expected Outcomes:**

1.A fully preprocessed and clean dataset ready for model training.

2.A trained classification model capable of identifying various types of network attacks.

3.A performance evaluation report of the model using key metrics like accuracy, precision, recall, and F1-score. This will tell us how good our model is at correctly identifying attacks without raising false alarms.

**2.Download and explore the NSL-KDD or CICIDS2017 dataset.**

For this project, you can choose one of two popular datasets. The CICIDS2017 is more modern and complex, while the NSL-KDD is a refined version of a classic benchmark dataset.I chosen CICIDS2017 dataset

*CICIDS2017:* A comprehensive dataset with labeled network flows, including recent attack types.

*Download:* Dataset:https://www.unb.ca/cic/datasets/ids-2017.html

*Exploration* involves loading the data (e.g., into a Pandas DataFrame in Python) and using functions like .head(), .info(), and .shape to get a first look at the rows, columns, and data types.

**3.Understand dataset structure and attack types.**

Before cleaning the data, you need to understand what each piece of information represents.

*Dataset Structure:* CICIDS2017 is much larger, with over 80 features extracted from network traffic flows, such as flow duration, packet lengths, and flags.

*Attack Types:* The data is labeled with different attack categories.

CICIDS2017 includes more modern attacks like Brute Force SSH, DoS, Heartbleed, Web Attacks, and Botnets.

**4.Perform basic statistics and data validation.**

*Basic Statistics:* Use functions like .describe() to get a summary of numerical features (mean, standard deviation, min/max values).This is crucial for identifying class imbalance, where you have far more examples of one class than another.

*Data Validation:* Look for anomalies. Are there any negative values for time duration? Do any features have zero variance (all values are the same)? This initial check helps spot data entry errors or irrelevant columns early on.

## Week-2 Data Cleaning and Preprocessing

Raw data is rarely ready for a machine learning model. This week focuses on refining the dataset into a clean, properly formatted state.

**1.Handle missing values, duplicates, and irrelevant features.**

Missing Values:Real-world data often has gaps. Common strategies include filling missing values with the mean, median, or mode of the column. If a row or column has too many missing values, it might be better to remove it entirely.

Duplicates: Duplicate rows can bias your model. They should be identified and removed to ensure each data point is unique. In Pandas, this is easily done with .drop_duplicates().

Irrelevant Features: Some features might not contribute any useful information for prediction. For example, a column where every value is identical has zero variance and can be safely dropped.

**2.Convert categorical features using encoding techniques.**

Machine learning models require numerical inputs, so text-based categorical features (like 'label') must be converted.I used label encoding technique for this

Label Encoding: This method assigns a unique integer to each category. This is simpler but can sometimes mislead models by implying an ordinal relationship where none exists.

**3.Normalize or standardize numerical features.**
Features often exist on vastly different scales. Scaling brings them to a common range, which helps many algorithms perform better.

*Normalization (Min-Max Scaling):* Rescales features to a specific range, typically [0, 1].

The formula is:$$x_{scaled} = \frac{x - x_{min}}{x_{max} - x_{min}}.

*Standardization:* Rescales features to have a mean of 0 and a standard deviation of 1. This is generally preferred as it is less sensitive to outliers.

The formula is:$$z = \frac{x - \mu}{\sigma}$$where
$\mu$ is the mean and $\sigma$ is the standard deviation.

**4.Split the dataset into training and testing sets.**

This is one of the most critical steps for evaluating your model properly.

*Why Split?* You train the model on one portion of the data (the training set) and then evaluate its performance on a separate, unseen portion (the testing set). This simulates how the model would perform on new, real-world data.

*How to Split?* A common split is 80% for training and 20% for testing. It's crucial to shuffle the data before splitting to ensure both sets are representative of the overall data distribution. Libraries like scikit-learn have functions (train_test_split) that handle this process easily.
