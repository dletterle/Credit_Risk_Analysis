# Credit_Risk_Analysis

# Overview 

Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

In order to accomplish this task, the following deliverables will be met: 
  * Deliverable 1: Use Resampling Models to Predict Credit Risk
  * Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
  * Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
  * Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)

# Results

**Naive Random Oversampling**

The Naive Random Oversampling method used RandomOverSampler to resample the data and enlarge the minority class of training data to use in a logistic regression model. The logistic regression model was trained and the following image and information refers to the resulting balanced accuracy score, confusion matrix, and classification report.
 * The model predicted the credit risk accurately 62.6% of the time
 * The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans
 * The recall scores for this model show that the model is better at identifying positive low-risk loans (0.67) and slightly lower at identifying high-risk loans (0.59) 

<img width="569" alt="image" src="https://user-images.githubusercontent.com/99268646/172733896-f053c5aa-59a1-49b5-ad13-2e4c521a34af.png">


**SMOTE Oversampling**

The SMOTE Oversampling method used SMOTE to resample the data and enlarge the minority class of training data to use in a logistic regression model.
 * The model predicted the credit risk accurately approximately 63% of the time
 * The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
 * The recall for both low and high risk loans were around 63%, meaning that the model found all positive instance 63% of the time. This is not a great score when trying to identify high-risk loans.

<img width="572" alt="image" src="https://user-images.githubusercontent.com/99268646/172734798-3f49fb15-a54c-4991-bf3a-d66cd120757e.png">


**Undersampling**

The Undersampling method used Cluster Centroids to resample the data and reduce the majority class of training data to use in a logistic regression model.
 * The model predicted the credit risk accurately only at approzimately 51%
 * The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
 * The recall scores for the high-risk loans were around 0.59 and the recall scores for low-risk loans were around 0.43. While the high-risk recall is much better, both recall scores are low and show that many of the positives were not accurately predicted

<img width="424" alt="image" src="https://user-images.githubusercontent.com/99268646/172735240-a2a3630b-b722-469a-9977-85f568681c6f.png">







