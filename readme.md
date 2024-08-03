Fraud Detection Project

Project Overview

This project focuses on detecting fraudulent transactions using a dataset with various transaction features. We conducted extensive exploratory data analysis (EDA), data preparation, and applied both clustering and classification techniques to identify and predict fraudulent activities. The dataset contains categorical and numerical features, including a label indicating whether a transaction is fraudulent.

Dataset

Rows: 106,036
Columns: 92 (after processing)
Key Features: source_prefix, dest_prefix, agent, status, amount, hour, among others.
Label: Binary variable indicating fraud (1) or normal transaction (0).

Project Structure

Exploratory Data Analysis (EDA)

Checked for missing values and data types.
Visualized the distribution of numerical features and the imbalance in the target variable.
Investigated the relationship between different features and the fraud label.

Data Preparation

Converted categorical variables into numerical format using one-hot encoding.
Scaled the amount feature for consistency.
Split the dataset into train and test sets using stratified sampling (80% train, 20% test).
Addressed class imbalance in the training set using the SMOTE technique.

Clustering with KMeans

Applied the KMeans algorithm to identify potential patterns in the data.
Used Grid Search to optimize the hyperparameters, particularly the number of clusters.
Assessed the model using metrics like precision, recall, F1-score, and confusion matrix, while considering the dataset's imbalance.

Classification with XGBoost

Applied XGBoost, a powerful classification algorithm, to predict fraud.
Conducted hyperparameter tuning using Grid Search.
Evaluated model performance with precision, recall, F1-score, accuracy, and ROC/AUC.
Implemented a threshold adjustment strategy to handle the low fraud rate (3.5%).

Results Visualization

Generated visualizations for confusion matrices, ROC curves, and other relevant plots to assess model performance.
Analyzed feature importance for fraud prediction.

Key Findings

EDA Insights: Most transactions are concentrated in a specific month, with noticeable peaks in fraudulent transactions during particular hours.

Clustering Analysis: The KMeans model was able to group similar transactions, but the clustering approach was less effective due to the high imbalance in the data.

Classification Results: The XGBoost classifier, tuned with Grid Search, provided robust predictions, with a strong focus on precision and recall due to the project's nature. Adjusting the decision threshold further improved the detection of fraudulent transactions.

Conclusion

This project successfully demonstrates a comprehensive approach to fraud detection using both unsupervised and supervised learning techniques. The detailed EDA and careful data preparation steps ensured a robust foundation for model building. The combination of clustering and classification techniques, along with appropriate evaluation metrics, provided valuable insights into detecting fraudulent transactions.

How to Use

Installation

Clone the repository.
Create a virtual environment and install the required packages (refer to requirements.txt).
Data Preparation

Load the dataset and follow the data preprocessing steps outlined in the notebooks.
Model Training and Evaluation

Run the scripts to train the KMeans and XGBoost models.
Evaluate model performance using the provided metrics and visualizations.
Contact
For any questions or issues, please contact Ali Abdi at abdi1373ali@gmail.com.