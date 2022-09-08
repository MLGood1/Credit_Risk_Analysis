# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to use the imbalanced-learn and scikit-learn libraries to resample credit card credit data from Lending Club.  The first objective was to oversample the data using RandomOverSampler and SMOTE alogrithms, then I used the ClusterCentroids algorithm to undersample the data, then use the SMOTEENN alogrithm to combine over and undersampling.  Lastly, I compared two ensemble learner models, the BalancedRandomForestClassifier and EasyEnsembleClassifier, alogrithms to further predict credit risk.

## Results

### Oversampling
1. RandomOverSampler Algorithm

![image](https://user-images.githubusercontent.com/104471775/188996889-aae408bc-7336-44aa-9356-e57e9630d49e.png)

![image](https://user-images.githubusercontent.com/104471775/188998163-ee6e8958-0736-44c7-82e6-6ba04f0f9eaa.png)

* This model has an accuracy rate of 66%.
* This model has a precision rate of 1% when predicting high risk credit, while predicting low risk credit at 100%.
* This model has a higher sensitivity (recall) to predicting high risk credit at 69%.
* This model has a low F1 score when it comes to predicting the high risk credit, indicating that there is a noticeable imbalance between 
precision and sensitivity.

2. SMOTE

![image](https://user-images.githubusercontent.com/104471775/189001822-a2f7e92b-6f2d-4b2f-ae73-f29cdb49051f.png)

![image](https://user-images.githubusercontent.com/104471775/189001870-b1681f64-b658-4a79-90f0-e86281946060.png)

* This model has an accuracy rate of 65%.
* Like the RandomOverSampler model, this model predicts high risk credit with a precision of 1%, while predicting low risk credit at 100%.
* This model has a higher sensitivity (recall) to predicting high risk credit at 61%.  The low risk credit has a sensitivity of 68%.
* This model has a low F1 score when it comes to predicting the high risk credit, indicating that there is a noticeable imbalance between 
precision and sensitivity.


### UnderSampling
1. ClusterCentroids

![image](https://user-images.githubusercontent.com/104471775/189021154-b0aa9c7e-4686-461b-b7e2-a67aea5d414e.png)

![image](https://user-images.githubusercontent.com/104471775/189021195-3a005fa8-7e24-422d-b88f-5b010380b0ea.png)

* This model has an accuracy rate of 54%.
* This model predicts high risk credit with a precision of 1%, while predicting low risk credit at 100%.
* This model has a higher sensitivity (recall) to predicting high risk credit, at 69%. The low risk credit has a sensitivity of 40%.
* This model has a low F1 score when it comes to predicting the high risk credit, indicating that there is a noticeable imbalance between 
precision and sensitivity.


### Combined Over and Under Sampling
1. SMOTTEN

![image](https://user-images.githubusercontent.com/104471775/189021462-70b0ca96-ce48-4701-90ee-a3444bfbf3a0.png)

![image](https://user-images.githubusercontent.com/104471775/189021554-c9ee33f0-289d-4dd5-bff3-4a23b8ce82f8.png)

* This model has an accuracy rate of 64%.
* This model predicts high risk credit with a precision of 1%, while predicting low risk credit at 100%.
* This model has a higher sensitivity (recall) to predicting high risk credit at 72%. The low risk credit has a sensitivity of 57%.
* This model has a low F1 score when it comes to predicting the high risk credit, indicating that there is a noticeable imbalance between 
precision and sensitivity.


### Ensemble Learners
1. Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/104471775/189022434-eac50908-4680-4774-b4c0-c67006bbe8cf.png)

![image](https://user-images.githubusercontent.com/104471775/189022482-3c4e3a7e-85c2-4e8b-9a80-e194a27d4e7a.png)

* This model has an accuracy rate of 68%.
* This model predicts high risk credit with a precision of 88%, while predicting low risk credit at 100%.
* This model has a sensitivity (recall) to predicting high risk credit at 37%. The low risk credit has a sensitivity of 100%.
* This model has a F1 score of 50% for high risk credit and 100% for low risk credit.  


2. Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/104471775/189022640-76bc29e7-6fb7-4539-8ab3-248fd1c5a6d0.png)

![image](https://user-images.githubusercontent.com/104471775/189022707-26dcbc62-4162-431c-9825-bf199ec90ee8.png)

* This model has an accuracy rate of 93%.
* This model predicts high risk credit with a precision of 9%, while predicting low risk credit at 100%.
* This model has a sensitivity (recall) to predicting high risk credit at 92%. The low risk credit has a sensitivity of 94%.
* The average F1 score is 97%.  The F1 score for high risk credit is at 16% and indicates that when predicting high risk credit there
is an imbalance between sensitivity and precision.

## Summary

All six models had a reasonably good accuracy score, ranging between 50% and 90% accurate.  However both over sampling models, the under sampling model,
and the combined sampling models where imbalanced toward sensitivity when predicating high risk credit resulting in a lot of false positives.  The ensemble learners were better balanced in precision and sensitivy.  While the EasyEnsemble Classifier had a higher accuracy rate (93%), I would recommend using the Balanced Random Forest Classifier.










