<h1 align="center"> Network Intrusion Detection System (NIDS) using Machine Learning</h1>

---

<h2> Project Overview</h2>

<p>
This project focuses on developing a <b>Network Intrusion Detection System (NIDS)</b> that leverages 
<b>supervised machine learning algorithms</b> to identify and classify network attacks. 
Using benchmark datasets like <b>NSL-KDD</b> or <b>CICIDS2017</b>, 
the system aims to detect malicious network activity and enhance cybersecurity awareness.
</p>

---

<h2> Milestone 1: Data Preparation</h2>

<h3>Week 1 – Project Initialization and Dataset Acquisition</h3>

<b>Objectives:</b>
<ul>
<li>Define project goals and expected outcomes.</li>
<li>Download and explore the <b>NSL-KDD</b> or <b>CICIDS2017</b> dataset.</li>
<li>Understand the dataset’s structure, attributes, and attack types.</li>
<li>Perform <b>basic statistical analysis</b> and <b>data validation</b>.</li>
</ul>

<b>Deliverables:</b>
<ul>
<li>Dataset acquired and verified.</li>
<li>Exploratory data analysis report.</li>
<li>Documentation of dataset insights and statistics.</li>
</ul>

---

<h3>Week 2 – Data Cleaning and Preprocessing</h3>

<b>Objectives:</b>
<ul>
<li>Handle <b>missing values</b>, <b>duplicates</b>, and <b>irrelevant features</b>.</li>
<li>Apply <b>encoding techniques</b> for categorical features.</li>
<li><b>Normalize</b> or <b>standardize</b> numerical columns.</li>
<li>Split the dataset into <b>training</b> and <b>testing</b> sets.</li>
</ul>

<b>Deliverables:</b>
<ul>
<li>Cleaned dataset ready for model training.</li>
<li>Encoded and normalized feature set.</li>
<li>Train-test split summary.</li>
</ul>

---

<h2>Milestone 2: Feature Engineering and Model Development</h2>

<h3>Week 3 – Feature Engineering and Selection</h3>

<b>Objectives:</b>
<ul>
<li>Analyze <b>feature importance</b> to determine key indicators.</li>
<li>Use <b>correlation analysis</b> or <b>PCA</b> for dimensionality reduction.</li>
<li>Create new derived features if beneficial.</li>
</ul>

<b>Deliverables:</b>
<ul>
<li>Finalized list of top features.</li>
<li>Visualization of feature relationships.</li>
<li>Documentation of feature selection methods.</li>
</ul>

---

<h3>Week 4 – Supervised Model Training</h3>

<b>Objectives:</b>
<ul>
<li>Train supervised ML models such as <b>Random Forest</b>, <b>SVM</b>, and <b>Logistic Regression</b>.</li>
<li>Evaluate performance using:</li>
<ul>
<li><b>Accuracy</b></li>
<li><b>Precision</b></li>
<li><b>Recall</b></li>
<li><b>F1-score</b></li>
</ul>
</ul>

<b>Deliverables:</b>
<ul>
<li>Trained model files.</li>
<li>Performance evaluation reports.</li>
<li>Comparison of model metrics.</li>
</ul>

---

<h2> Final Evaluation and Model Comparison</h2>

<p>
Three supervised machine learning models—<b>Random Forest</b>, <b>Support Vector Machine (SVM)</b>, 
and <b>Logistic Regression</b>—were evaluated using the top 10 most significant features identified via 
Random Forest feature importance.
</p>

<h3>Random Forest</h3>
<ul>
<li><b>Accuracy:</b> 99.81%</li>
<li>Delivered outstanding performance across all classes.</li>
<li>Demonstrated high consistency and robustness.</li>
<li>Most reliable model for real-world intrusion detection.</li>
</ul>

<h3>Support Vector Machine (SVM)</h3>
<ul>
<li><b>Accuracy:</b> 94.46%</li>
<li>Captured complex nonlinear patterns effectively.</li>
<li>Slightly lower performance in minority classes.</li>
<li>Suitable for balanced datasets with moderate complexity.</li>
</ul>

<h3>Logistic Regression</h3>
<ul>
<li><b>Accuracy:</b> 91.76%</li>
<li>Reliable for dominant classes but weaker for minority ones.</li>
<li>Excellent baseline model with interpretability and simplicity.</li>
</ul>

<p><b>Summary:</b>  
All three models showed strong performance, confirming the quality of data preprocessing and feature selection.  
Among them, <b>Random Forest</b> achieved the best accuracy, precision, and scalability, 
making it ideal for production-level network intrusion detection.</p>

---

<h2> Technologies Used</h2>

<table>
<tr><th>Category</th><th>Tools</th></tr>
<tr><td><b>Language</b></td><td>Python</td></tr>
<tr><td><b>Libraries</b></td><td>Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn</td></tr>
<tr><td><b>Datasets</b></td><td>NSL-KDD / CICIDS2017</td></tr>
</table>

---
<h2> Milestone 3 & 4 – Weekly Implementation Details </h2>
<h3> Week 5: Anomaly Detection with Unsupervised Learning </h3> <p> In Week 5, the focus was on implementing <b>unsupervised learning techniques</b> to identify abnormal network traffic without relying on labeled data. Algorithms such as <b>K-Means Clustering</b> and <b>Isolation Forest</b> were applied to detect deviations from normal behavior. Dimensionality reduction using <b>PCA</b> was performed to understand anomaly separation patterns. </p> <ul> <li>Applied K-Means and Isolation Forest for anomaly detection.</li> <li>Identified abnormal traffic behaviors using clustering outputs.</li> <li>Calculated anomaly ratios and cluster purity.</li> <li>Analyzed PCA-based visual separation of normal vs anomalous flows.</li> </ul> <p><b>Deliverables:</b> Unsupervised anomaly detection models, anomaly analysis report, and detailed documentation of findings.</p>
<h3> Week 6: Model Evaluation and Fine-Tuning </h3> <p> This week involved evaluating all models—both supervised and unsupervised—and improving their performance using <b>hyperparameter tuning</b>. Techniques like <b>GridSearchCV</b> and <b>RandomizedSearchCV</b> were used to optimize accuracy, recall, and F1-score. Comprehensive evaluations such as confusion matrices and ROC curves were generated to compare models. </p> <ul> <li>Compared performance of Random Forest, SVM, Logistic Regression, K-Means, and Isolation Forest.</li> <li>Performed hyperparameter tuning using GridSearchCV and RandomizedSearchCV.</li> <li>Generated confusion matrix, ROC curve, and classification reports.</li> <li>Selected final optimized model for deployment.</li> </ul> <p><b>Deliverables:</b> Optimized machine learning model, complete evaluation metrics, and final model selection documentation.</p>
<h3> Week 7: Alert Generation and Logging </h3> <p> In Week 7, a <b>real-time intrusion alert system</b> was developed. The best-performing model was used to simulate real-time predictions and generate alerts for detected intrusions. Each alert was logged with timestamps, attack category, and model confidence score. Logs were stored in CSV and text formats to allow easy integration with dashboards or monitoring tools. </p> <ul> <li>Simulated real-time intrusion detection using test data.</li> <li>Developed alert-generation logic for identified attacks.</li> <li>Logged alerts with timestamp, attack type, and confidence score.</li> <li>Stored results in CSV and text formats.</li> </ul> <p><b>Deliverables:</b> Real-time alert generation module, structured intrusion logs, and alert workflow documentation.</p>
<h2> Project Timeline Summary</h2>


---





