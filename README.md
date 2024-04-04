In the Dataset, we are using a "Maternal Health Risk Dataset," and we found it from 'Kaggle' platform. 
The dataset contains information of 1014 Patients. Altogether, the data has got seven columns for each of the patients. 
Each patient has got the data consisting of their Age, Systolic BP (Blood Pressure), Diastolic BP (Blood Pressure), BS (Blood Sugar), Body Temperature, Heart Rate and Risk level.
Most of the Data are Continuous Data in the dataset. A continuous Data is a dataset where the numericals are continuous in nature and can take on any value within a certain range.
If the data had been collected directly from patients, it would have been collected in Numerical data type. A "Numerical data type" is described as the data types that are applied to represent numeric values. 
The “df.isnull().sum()” is a Pandas Series where each element represents the count of missing values in the corresponding column of the original Data Frame. 
we have no null values present in the dataset. Hence, there is no data cleaning required for the dataset.
The df.describe() method in Python's pandas library generates descriptive statistics for Numerical columns DataFrame. 
The "df.shape" attribute is used for the purpose of obtaining the dimensions of a Data Frame. 
The df.sample() method in Pandas is used to obtain a random sample of rows from a Data Frame and It returns a single random row.
The 'df["HeartRate"].hist()' attribute generates a histogram to visualize the distribution of heart rates stored in "HeartRate" column of pandas DataFrame (df).
The 'counts = df['RiskLevel'].value_counts()' attribute is used to calculate counts for each category.
The 'plt.pie(counts, labels=counts.index, autopct='%1.1f%%', startangle=90)' is used to create a pie chart.
The 'plt.axis('equal')' attribute ensures that the piechart is drawn as a circle.
The 'plt.show()' is used to display the chart.
The 'df["RiskLevel"].value_counts()' this attribute counts the occurence of each value in the 'RiskLevel' column.
The 'sns.barplot(x=df["RiskLevel"],y=df["HeartRate"])' this attribute creates a barplot to visualize the relationship between 'RiskLevel' and 'HeartRate' stored in dataFrame 'df'.
The 'sns.barplot(x=df["RiskLevel"],y=df["BS"])' this attribute creates a barplot to visualize the relationship between 'RiskLevel' and 'BS' stored in DataFrame 'df'.
The 'sns.barplot(x=df["RiskLevel"],y=df["Age"])' this attribute creates a barplot to visualize the relationship between 'RiskLevel' and 'Age' stored in DataFrame 'df'.
The standard deviation has a higher value that is because the patients have an age span of 10 to 70 years. 

Random Forest Classifier Model:
# Code Explanation
- Initialize Model:
  We initialize a Random Forest classifier model with 100 estimators and set the random state to 42.

- Train the Model:
  The model is trained using the `fit()` method on the training data (`X_train` and `y_train`).

- Make Predictions:
  Predictions are made on the test set using the trained model (`rf_model.predict(X_test)`).

- Evaluate the Model:
  We evaluate the model's performance using metrics such as accuracy, confusion matrix, and classification report.

# Results:
- Accuracy:
  The accuracy of the model on the test set is printed as a percentage.
  
- Confusion Matrix:
  The confusion matrix provides a summary of the model's performance in terms of true positive, true negative, false positive, and false negative predictions.

- Classification Report:
  The classification report includes precision, recall, F1-score, and support for each class.
The Random Tree Model achieved an accuracy of approximately 81.28%.

 Decision Tree Classifier Model:
 The decision tree classifier is a powerful machine learning algorithm for solving classification problems.
 # Code Explanation:
- Initialize Decision Tree Model:
  The DecisionTreeClassifier model is initialized with a specified random state for reproducibility.

- Train the Model:
  The initialized decision tree model is trained using the training data (X_train and y_train).

- Make Predictions:
  Predictions are made on the test set (X_test) using the trained model.

- Evaluate the Model:
  We evaluate the model's performance using metrics such as accuracy, confusion matrix, and classification report.
- Accuracy Calculation: The accuracy of the model is calculated using accuracy_score.
- Confusion Matrix: Confusion matrix is computed using confusion_matrix.
- Classification Report: Classification report containing precision, recall, F1-score, and support is generated using classification_report.
  
# Results:
  The accuracy, confusion matrix, and classification report are printed to the console for analysis.
The Decision Tree Model achieved an accuracy of approximately 81.77%.  

The Random Forest Model demonstrates a strong performance on the test set, achieving an accuracy of approximately 81.28%.
The model demonstrates a favorable ability to predict labels correctly, as given by evaluation metrics, including the confusion matrix and classification report. 


