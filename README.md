![image](https://github.com/NTHub23/credit-risk-classification/assets/138403390/c5aa92b6-47e3-4bae-b16c-b3ecf147917e)

# Credit Risk Classification

In this Challenge,  various techniques were used to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was used to build a model that can identify the creditworthiness of borrowers.

## Instructions
The instructions for this Challenge was divided into the following subsections:

- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Predict a Logistic Regression Model with Resampled Training Data

- Write a Credit Risk Analysis Report - Credit Risk Analysis Report

## Split the Data into Training and Testing Sets
Opened the starter code notebook and used it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

1.  Created the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
   
2. Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

    > **Note** A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

3. Check the balance of the labels variable (`y`) by using the `value_counts` function.

4. Split the data into training and testing datasets by using `train_test_split`.


## Create a Logistic Regression Model with the Original Data
1. Fit a logistic regression model by using the training data (`X_train` and `y_train`).

2. Saveed the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.

3. Evaluated the model’s performance by doing the following:

    * Calculate the accuracy score of the model.

    * Generate a confusion matrix.

    * Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

### Predict a Logistic Regression Model with Resampled Training Data

Noticed a small number of high-risk loan labels? Perhaps, a model that uses resampled data will perform better. Thus resampled the training data and then reevaluated the model. Specifically, useing `RandomOverSampler`.

To do so, complete the following steps:

1. Used the `RandomOverSampler` module from the imbalanced-learn library to resample the data. Making sure to confirm that the labels have an equal number of data points.

2. Used the `LogisticRegression` classifier and the resampled data to fit the model and made predictions.

3. Evaluated the model’s performance by doing the following:

    * Calculated the accuracy score of the model.

    * Generated a confusion matrix.

    * Printed the classification report.

4. Answered the following question: How well does the logistic regression model, fit with oversampled data, predict both the `0` (healthy loan) and `1` (high-risk loan) labels?
   
## Write a Credit Risk Analysis Report

Wrote a brief report that included a summary and analysis of the performance of the machine learning models that was used in this homework. 

## Summary : 
## Question: 
### How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
The logistic regression model performs exceptionally well for class 0(healthy loan), achieving high precision, recall and F1-score.

For class 1 (high risk loan), the model shows good performance, but there is some room for improvement, especially in terms of precision.

Overall, the model has high accuracy and performs well across the majority and minority classes.

## Question: 
### How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Answer: Both models perform very well, with high accuracy, precision, recall, and F1-score. The original model has a slightly higher precision for class 1, but the oversampled model has a higher F1-score for class 1, indicating a better balance between precision and recall. Depending on the specific requirements and goals for classification task, one choose one model over the other based on the trade-off between precision and recall for class 1.
