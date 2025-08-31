Diabetes Prediction Model ->
This repository contains a machine learning project that predicts the onset of diabetes based on diagnostic measurements. The model uses Logistic Regression and follows a complete data science workflow, from data cleaning and preprocessing to model evaluation and saving.

​Project Overview ->
​The main objective of this project is to build a reliable predictive model that can identify individuals at risk of diabetes. The process is broken down into four key stages:

​1)  Data Cleaning and Preprocessing :
​The initial step involved cleaning the raw dataset. This was necessary because several features, such as BloodPressure and Insulin, contained medically impossible zero values. To handle these, median imputation was used to replace the zeros, ensuring the integrity of the data.
​Furthermore, we identified and handled outliers in the dataset, particularly in the Insulin feature. A quantile-based approach was used to remove extreme values that could skew the model's performance. The effect of this cleaning is visible in the improved data distribution shown in the box plots.

​2) Handling Imbalanced Data :
​The dataset was found to be imbalanced, with a significantly larger number of non-diabetic cases than diabetic ones. To prevent the model from becoming biased towards the majority class, we applied SMOTE (Synthetic Minority Over-sampling Technique). SMOTE generates synthetic data points for the minority class, effectively balancing the dataset and improving the model's ability to correctly identify diabetes cases.

​
3) Model Training and Evaluation :
​The prepared data was split into training and testing sets. A Logistic Regression model was trained on the training set and evaluated on the test set. The model's performance was measured using a confusion matrix  and key metrics:
​- Accuracy: The overall proportion of correct predictions.
​- Precision: The ratio of true positive predictions to all positive predictions.
​- Recall: The ratio of true positive predictions to all actual positive cases. Recall is particularly important in medical contexts, as it measures the model's ability to find all positive instances.
​- F1-Score: The harmonic mean of precision and recall, providing a balanced measure of the model's performance.

​4) Saving the Model :
​The final, trained model was saved using the pickle library. This allows the model to be easily loaded and used for future predictions without needing to be retrained, which is also a crucial step for deploying the model.
