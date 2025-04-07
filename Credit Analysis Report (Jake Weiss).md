# Module 20 Report 

## Overview of the Analysis

* **Purpose of the  Analysis** - The purpose of the analysis was to see if the the logistic regression model can predict loan health accurately using the original dataset or a resampled dataset.
* **Explain what financial information the data was on, and what you needed to predict.** -The dataset provided information on 77,536 loans, with 75,036 of them being healthy loans and 2,500 of them being high-risk loans. The dataset consists of 8 columns: loan size, interest rate, borrower income,, debt to income, number of accounts, derogatory marks,  total debt, and finally loan status. Loan status is what we are ultimately attempting to predict, and we're using the other columns to inform our model and make predictions based on the data.

* **Describe the stages of the machine learning process you went through as part of this analysis.** 
	* **First:** I read the `lending_data.csv file`, and put it into a Pandas DataFrame.
	*  **Second:** I separated the data into labels and features. The labels are what I'm trying to predict. So the label is the loan status column which is binary column that shows a '0' for a healthy loan and a '1' for a high-risk loan. Features is all the other data that I will use to train the model.
	*  **Third:** I checked the balance of the labels, to see what the spread of 0s and 1s looked like, and saw it mostly 0s (healthy loans).
	*  **Fourth:** I split the data into training and testing data sets using `train_test_split`.
	*  **Fifth:** I imported the LogisticRegression module from SKLearn and fit a logistic model regression by using the training data.
	*  **Sixth:** I used the model to make predictions using the testing data, and evaluated said predictions. Via generating an accuracy score, a confusion matrix, and finally a classification report.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: - Logistic Regression
	  *  **Accuracy Score:** 99%
	  *  **Precision Scores:**
			  * Healthy loans: 100%
			  * High-Risk loans: 84%
		* **Recall Scores:**
			* Healthy loans: 99%
			* High-Risk loans: 94% 



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary


**Question:**  How well does the logistic regression model predict both the  `0`  (healthy loan) and  `1`  (high-risk loan) labels?

**Answer:**  It does a great job at prediciting  `0`  (healthy loans) with 100% accuracy it didn't miss a healthy loan. It does a adequate job at predicting  `1`  (high-risk loans) with 84% accuracy. Which means that every loan that was flagged as high-risk was truly high-risk, but some loans that were flagged as healthy were actually high-risk. At the same time no loan that was genuinely healthy was accidently flagged as high-risk. The overall accuracy of the model was 99%
