# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to use the imbalanced-learn and scikit-learn libraries to resample credit card credit data from Lending Club.  The first objective was to oversample the data using RandomOverSampler and SMOTE alogrithms, then I used the ClusterCentroids algorithm to undersample the data, lastly I used the SMOTEENN alogrithm to combine over and undersampling.  Lastly, I compared the BalancedRandomForestClassifier and EasyEnsembleClassifier alogrithms to predict credit risk.

## Results

### Oversampling
1. RandomOverSampler Algorithm

![image](https://user-images.githubusercontent.com/104471775/188996889-aae408bc-7336-44aa-9356-e57e9630d49e.png)

![image](https://user-images.githubusercontent.com/104471775/188998163-ee6e8958-0736-44c7-82e6-6ba04f0f9eaa.png)

* This model has an accuracy rate of 66%.
* This model has a precision rate of 1% when predicting high risk credit, while predicting low risk credit at 100%.
* This model has a higher sensitivity (recall) to predicting low and high risk credit, at 62% and 69%, respectively.

2. SMOTE

![image](https://user-images.githubusercontent.com/104471775/189001822-a2f7e92b-6f2d-4b2f-ae73-f29cdb49051f.png)

![image](https://user-images.githubusercontent.com/104471775/189001870-b1681f64-b658-4a79-90f0-e86281946060.png)




