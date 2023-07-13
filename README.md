Email Classification using Common Machine learning Model with Bootstrap Confidence Intervals and Other Evaluation Metric
Introduction: The goal of this project was to develop a machine learning model for email classification into spam and ham categories. The dataset used for training and evaluation contained email messages labeled with their respective categories. The approach involved using
logistic regression as the classification algorithm and employing
Method: Bootstrap resampling to estimate confidence intervals for the Spam Email s performance metrics.
1. Data Preparation:
a. The dataset was read into a Pandas Data Frame, which consisted of two columns: Category and Message.
b. Preprocessing steps, such as removing non-text emails, were applied to clean the dataset.
c. The Category column was encoded, assigning the value 1 for ham emails and 0 for spam emails.
2. Training and Testing Data Split:
a. The dataset was divided into training and test sets using the train_test_split function from scikit-learn.
b. The training set comprised 80% of the data, while the remaining 20% was used
for testing.
3. Feature Extraction:
a. b. c.
Text data was transformed into numerical feature vectors using the TF-IDF vectorization technique.
The TfidfVectorizer class from scikit-learn was utilized, considering parameters such as minimum document frequency, stop words, and lowercase conversion. The training set was transformed into feature vectors using the fit_transform method, and the test set was transformed using transform.
Model Application:
1. Logistic Regression:
• Training Accuracy: 0.9670
• Training Precision: 0.9643
• Training Recall: 0.9990
• Test Accuracy: 0.9094
• Test Precision: 0.9048
• Test Recall: 1.0000
• Accuracy Confidence Interval: [0.02421525 0.04484305]
2. K-Nearest Neighbors (KNN):
• Training Accuracy: 0.9201
• Training Precision: 0.9159
• Training Recall: 0.9997
• Test Accuracy: 0.9094
• Test Precision: 0.9048
• Test Recall: 1.0000
• Accuracy Confidence Interval: [0.89237668 0.92556054]
3. Lasso Regression Training Accuracy:
• Accuracy: 0.8609865470852018
• Precision: 0.8609865470852018
• Recall: 1.0
• F1-Score: 0.9253012048192771
• Accuracy Confidence Interval: [0.83946188 0.88161435]
Conclusion:
In this project, we developed machine learning models for email classification into spam and ham categories. Logistic regression, K-nearest neighbors (KNN), and Lasso regression were applied as the classification algorithms. The models achieved decent performance with respect to accuracy, precision, and recall on both the training and test data. Furthermore, bootstrap resampling was employed to estimate confidence intervals for the accuracy metric, providing a measure of the model's stability. The confidence intervals obtained through resampling provide valuable insights into the variability of the model's performance. Based on the results, it can be concluded that both logistic regression and KNN models performed similarly well in terms of
accuracy, precision, and recall. However, the Lasso regression model showed slightly lower performance in terms of accuracy but achieved a higher F1-score. Overall, this project demonstrates the effectiveness of machine learning models in email classification tasks and highlights the importance of evaluating model performance using appropriate evaluation metrics and estimating confidence intervals to assess the model's stability.
