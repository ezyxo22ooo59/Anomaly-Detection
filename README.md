# Anomaly-Detection

## Supervisor Model Project: Anomaly Detection in Loan Defaults
### Background and Usage
The financial sector is fraught with risks, particularly the risk of loan defaults, which can significantly impact the profitability and stability of financial institutions. Anomaly detection in this context involves identifying patterns and instances that deviate from the norm, such as loans that are likely to default. This project focuses on developing and evaluating supervised learning models to predict loan defaults using a rich dataset from XYZ Corporation, which includes various features related to loans, demographics, and financial metrics.

The primary usage of this project is to build predictive models that can accurately identify high-risk loans, thereby enabling financial institutions to take preemptive measures. By using machine learning techniques such as decision trees, gradient boosting, and deep learning, the project aims to enhance the accuracy of loan default predictions, ultimately contributing to better risk management and decision-making processes in financial institutions.

### Project Aspect
This project was undertaken to address a critical challenge in the financial sector: predicting loan defaults. The ability to accurately forecast which loans are at risk of default allows financial institutions to mitigate potential losses and make informed lending decisions. Additionally, the project serves as a comprehensive case study for applying advanced machine learning techniques to real-world financial data, showcasing the power of these methods in enhancing predictive analytics. 

Here are several aspects of this project stand out:

Comprehensive Approach:
- The project combines multiple machine learning techniques and thorough data analysis, providing a holistic approach to anomaly detection in loan defaults.

Interpretable Machine Learning:
- The use of SHAP values for feature importance and dependence analysis adds a layer of interpretability, making it easier to understand how different factors contribute to loan defaults.

Practical Application:
- The project addresses a real-world problem with significant implications for the financial sector, demonstrating the practical utility of machine learning in risk management.

Robust Validation:
- The use of cross-validation techniques ensures that the models are not only accurate but also robust and reliable.

Transferability:
- The code is designed to be adaptable, allowing other users to apply the methodologies to their own datasets with minimal adjustments.



### Key results

1. Model Performance:
- The Gradient Boosting model achieved a Root Mean Square Error (RMSE) of 0.383 and an R-squared value of 0.194.
- The Deep Learning model also performed well, with similar RMSE and R-squared values.
- The Decision Tree model without Weight of Evidence (WOE) encoding had an accuracy of 0.8096, while the model with WOE encoding had a slightly lower accuracy of 0.8052 but offered better interpretability.

2. Feature Importance:
- Analysis using SHAP (SHapley Additive exPlanations) values identified key features influencing loan default, such as education level (AP003), the count of P2P queries (TD009), and the number of months since loan origination (CR015).
- The feature importance plots and dependence plots provided deep insights into how each feature impacts the prediction, aiding in model -interpretability.

3. Cross-Validation:
- The project employed Leave-One-Out Cross-Validation (LOOCV) and 10-Fold Cross-Validation to ensure the robustness of the models. The estimated RMSE via LOOCV and 10-Fold CV provided additional validation of the model's performance.


### Code Usability
Other people can use the code from this project. The code is structured in a way that allows for easy adaptation and application to different datasets and scenarios. Here's how others can use it:

Data Preparation:
- Replace the dataset with their own financial data, ensuring it has similar features.
- Follow the data preprocessing steps provided in the code to clean and transform the data.

Model Training:
- Utilize the provided code to train decision tree, gradient boosting, and deep learning models.
Modify hyperparameters and model configurations as needed to suit their specific data and requirements.

Feature Engineering and Evaluation:
- Apply the feature engineering techniques and WOE encoding as demonstrated.
- Use the SHAP analysis code to interpret feature importance and understand model predictions.

Model Validation:
- Perform cross-validation to ensure the robustness of the models.
- Use the provided metrics and plots to evaluate model performance.

In conclusion, this project exemplifies the effective application of machine learning to a critical problem in the financial sector, providing valuable insights and tools that can be leveraged by other practitioners in the field.







## Unsupervised Model Project: Anomaly Detection in Healthcare Payments
### Background and Usage
Healthcare systems involve intricate billing processes, with numerous transactions occurring daily. Detecting anomalies in healthcare payments can help identify fraudulent activities, billing errors, and other irregularities. This project aims to develop unsupervised learning models to detect anomalies in healthcare payment data, specifically using the inpatient charges dataset.

The dataset used in this project, inpatientCharges.csv, contains various features related to healthcare providers, charges, and payments. The goal is to identify patterns and instances that deviate from the norm, indicating potential anomalies.

### Project Aspect
This project addresses a critical need in the healthcare sector: detecting anomalies in payment data to identify potential fraud, billing errors, and other irregularities. By applying unsupervised learning models, the project provides a robust approach to anomaly detection without relying on labeled data. This is particularly valuable in real-world scenarios where labeled data may be scarce or unavailable.

Several aspects of this project:

Comprehensive Approach:
- The project combines multiple unsupervised learning techniques and thorough data analysis to detect anomalies in healthcare payments.

Feature Engineering:
- The creation of new features, such as the average and ratio of payments, provides a deeper understanding of the data and enhances the effectiveness of anomaly detection.

Model Comparison:
- Comparing different models (HBOS, ECOD, PCA, and Autoencoder) provides valuable insights into their strengths and weaknesses, helping to choose the best approach for anomaly detection.

Practical Application:
- The project addresses a real-world problem with significant implications for the healthcare sector, demonstrating the practical utility of unsupervised learning in fraud detection and billing accuracy.

Transferability:
- The code is designed to be adaptable, allowing other users to apply the methodologies to their own datasets with minimal adjustments.

### Key Results
The project involved several steps, including data preparation, feature engineering, and applying different unsupervised learning models to detect anomalies.

1. Data Preparation and Feature Engineering:
- The dataset was loaded, and preliminary exploratory data analysis (EDA) was performed to understand the distribution and summary statistics of the data.
- New features were engineered, such as the average and ratio of total payments by each provider, and the average payments made by beneficiaries or third parties.
- These features helped create a comprehensive dataset that facilitated the detection of anomalies.

2. Model Building and Evaluation:
- Histogram-based Outlier Score (HBOS):
  - The HBOS model was applied to the dataset. It showed a contamination rate of 14.307, identifying 8150 outliers out of 163065 observations.
  - The model's threshold was set at 14.307, and observations with anomaly scores above this threshold were considered outliers.
  - The model effectively identified outliers, which was validated by a confusion matrix showing accurate classification of normal and outlier groups.
- Empirical Cumulative Distribution Functions (ECOD):
  - The ECOD model was applied, showing a contamination rate of 16.961, identifying 8154 outliers.
  - The threshold for this model was set at 16.961, with similar validation steps to ensure accuracy.
- Principal Component Analysis (PCA):
  - PCA was used to transform the data and identify anomalies based on the explained variance of principal components.
  - The model showed a contamination rate of 16.961, consistent with the ECOD model, and effectively identified outliers.
- Autoencoder:
  - An autoencoder neural network was trained to detect anomalies by learning the essential patterns of the data and identifying deviations.
  - The model achieved a stable loss and effectively identified anomalies in the dataset.
  
3. Model Comparison:
- The results from HBOS, ECOD, and PCA were compared to evaluate the effectiveness of each model.
- Cross-tabulations showed the overlap of outliers identified by different models, providing insights into their consistency and reliability.

### Code Usability
Other people can use the code from this project. The code is structured to allow easy adaptation and application to different datasets and scenarios. Here's how others can use it:

Data Preparation:
- Replace the dataset with their own healthcare payment data.
- Follow the data preprocessing and feature engineering steps to prepare the data for analysis.

Model Training:
- Utilize the provided code to train HBOS, ECOD, PCA, and Autoencoder models.
- Adjust model parameters and contamination rates as needed to suit their specific data.

Model Evaluation:
- Use the evaluation metrics and visualizations to assess model performance.
- Compare results from different models to determine the most effective approach for their data.

In conclusion, this project exemplifies the effective application of unsupervised learning to detect anomalies in healthcare payments, providing valuable insights and tools that can be leveraged by other practitioners in the field.



## Unsupervised Model Project: Anomaly Detection in Credit Card Transactions

### Background and Usage
In the realm of financial transactions, particularly those involving credit cards, the detection of anomalies is crucial to identify fraudulent activities, billing errors, and other irregularities. This project focuses on developing and enhancing features from a dataset containing credit card transactions to facilitate anomaly detection. The dataset, purchase_credit_card.csv, includes various transaction details such as dates, amounts, merchants, and cardholder information.

### Project Aspect
The objective of this project was to create robust features that facilitate the detection of anomalies in credit card transactions. Given the vast amount of transaction data, identifying patterns and irregularities manually is impractical. By leveraging feature engineering and unsupervised learning techniques, this project aims to enhance the efficiency and accuracy of anomaly detection in financial transactions. The insights gained can help financial institutions in preventing fraud, improving security, and maintaining trust with their customers.

Several aspects of this project:
Comprehensive Feature Engineering:
- The project goes beyond basic feature extraction, creating nuanced features that capture various dimensions of transaction behavior.

Use of Ratios and Comparisons:
- The use of ratios and comparisons to averages and medians provides a deeper understanding of the data, helping to highlight potential anomalies.

Practical Application:
- The project addresses a real-world problem with significant implications for financial security and fraud prevention.

Transferability:
- The methods and code are designed to be easily transferable to other datasets, making it useful for a wide range of anomaly detection tasks.

### Key Results
The project involves several key steps:

1. Data Import and Initial Exploration:
- The dataset was loaded using pandas and the initial structure was explored.
- The dataset consists of 442,458 records with 11 columns.

2. Data Preparation:
- Column names were standardized for ease of access.
- Additional columns were created for Year, Month, Week_Number, and Day_of_Week based on transaction dates.
- Descriptive statistics provided an overview of transaction amounts, highlighting potential outliers.

3. Feature Engineering:
- Feature 1: Ratio of Amount Spending to Mean Spending by Merchant Category:
  - Calculated the mean spending by each agency and merchant category.
  - Created a feature representing the ratio of each transaction amount to the mean spending.
- Feature 2: Ratio of Amount Spending to Median Spending by Merchant Category:
  - Similar to Feature 1, but using the median spending amount.
- Feature 3: Month Average by Merchant Category:
  - Calculated the average month of transactions for each agency and merchant category to identify seasonal patterns.
- Feature 4: Ratio of Month Average by Merchant Category:
  - Ratio of each transaction month to the average month for the same merchant category.
- Feature 5: Month Median by Merchant Category:
  - Similar to Feature 3, but using the median month.
- Feature 6: Ratio of Month Median by Merchant Category:
  - Ratio of each transaction month to the median month for the same merchant category.
- Feature 7: Spend Amount Mean for Each User:
  - Calculated the mean spending amount for each cardholder.
- Feature 8: Ratio of Spend Amount Mean for Each User:
  - Ratio of each transaction amount to the mean spending amount for the same cardholder.
- Feature 9: Spend Amount Median for Each User:
  - Calculated the median spending amount for each cardholder.
- Feature 10: Ratio of Spend Amount Median for Each User:
  - Ratio of each transaction amount to the median spending amount for the same cardholder.
- Feature 11: Spend Amount Max for Each User:
  - Calculated the maximum spending amount for each cardholder to identify unusually large transactions.
- Feature 12: Spend Amount Min for Each User:
  - Calculated the minimum spending amount for each cardholder to identify unusually small or negative transactions.
- Feature 13: Spend Amount Mean for Each Agency:
  - Calculated the mean spending amount for all transactions under each agency.
- Feature 14: Spend Amount Median for Each Agency:
  - Calculated the median spending amount for all transactions under each agency.
- Feature 15: Spend Amount Max for Each Agency:
  - Calculated the maximum spending amount for all transactions under each agency to identify unusually large transactions.

In conclusion, this project exemplifies the effective application of feature engineering to enhance anomaly detection in financial transactions, providing valuable insights and tools that can be leveraged by other practitioners in the field.









