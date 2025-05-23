# Fraudulent-detection

📌 Objective:
To build a machine learning model that detects fraudulent financial transactions and identifies patterns indicating fraudulent behavior. The goal is to improve detection accuracy and help financial institutions minimize fraud losses.

🗃️ Dataset Overview:
Source: Transactional data containing features of each transaction.

Key Columns:

step: Time step of the transaction.

type: Type of transaction (e.g., CASH_OUT, TRANSFER).

amount: Transaction amount.

nameOrig, nameDest: Sender and receiver identifiers.

oldbalanceOrg, newbalanceOrig: Sender’s balance before and after the transaction.

oldbalanceDest, newbalanceDest: Receiver’s balance before and after the transaction.

isFraud: Target variable (1 if fraudulent, 0 otherwise).

isFlaggedFraud: Indicates if the system flagged the transaction.

🔧 Data Preprocessing & Feature Engineering:
Handled Missing & Anomalous Values: Cleaned irrelevant or corrupted entries.

Engineered New Features:

balance_delta_orig = oldbalanceOrg - newbalanceOrig

balance_delta_dest = oldbalanceDest - newbalanceDest

These help measure sudden or suspicious changes in balances.

Encoded Categorical Variables: Converted transaction types to numeric form.

Scaling: Normalized numerical features to bring uniformity.

📊 Exploratory Data Analysis (EDA):
Analyzed class imbalance: Fraud cases are rare compared to normal transactions.

Studied transaction types with higher fraud probability (TRANSFER and CASH_OUT).

Observed abnormal balance patterns in fraud cases.

🧠 Model Building:
Tried multiple models to compare performance:

Logistic Regression

K-Nearest Neighbors (KNN)

Decision Tree

Support Vector Machine (SVM)

Addressed class imbalance using techniques like:

Oversampling (SMOTE)

Adjusting class weights

📈 Evaluation Metrics:
Used metrics suitable for imbalanced classification:

Precision, Recall

F1 Score

Confusion Matrix

ROC-AUC Score

Focused more on Recall to minimize false negatives (fraud missed).

🔍 Key Findings:
Most frauds occur in TRANSFER and CASH_OUT types.

Sudden drop in sender balance and unusual destination balances are good fraud indicators.

Tree-based models (like Decision Tree or Random Forest, if extended) tend to perform better in capturing nonlinear fraud patterns.

🏁 Outcome:
A deployed model capable of predicting fraud transactions with high recall.

Insights generated for improving infrastructure, such as transaction monitoring systems.
