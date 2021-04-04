# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

In this module challenge we are tasked with evaluating credit risks using 6 different types of machine learning techniques. These techniques are oversampling the data using random oversampling, SMOTE, undersampling using cluster centroid, using a combination of the two using SMOTEENN, and finally reducing bias using random forest classifier and easy ensemble classifier. By looking at the results of these different methods we are able to evaluate their usefulneses and applicability in future projects involving Credit Risk or similiar financial KPIs. 

## Results

### RandomOverSample Method:
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/RandomOversample/randomOversamp_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/RandomOversample/randomOverSampler_confusionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/RandomOversample/randomOversampler_classificationreport.JPG)

The accuracy score using RandomOverSample is 63.5%. The high risk precision is 1% at a 59% sensitivity giving us a f1 score of only .02. This is due to a small amount of low_risk population where we see the precision is around 100% and a sensitivty of 62%!


### SMOTE Method:
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTE/SMOTE_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTE/SMOTE_confussionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTE/SMOTE_classificationreport.JPG)

The accuracy score using the SMOTE method is 64.7%. The high risk precision is 1% at a 67% sensitiving giving us a f1 score of only .02. Once again ths is due to a small amount of low_risk population where we see a precision around 100% and a sensitivity of 63%. 


### UnderSampling ClusterCentroid Method:
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/clustercentroid/clustercentroid_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/clustercentroid/clustercentroid_confusionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/clustercentroid/clustercentroid_classificationreport.JPG)

Using the ClusterCentroid method we see a balanced accuracy score drop to 53%. The high risk precision remains at 1% with a sensitivity of 61% and our f1 score dropping to 1%. Low risk remains at 100% precision with a sensitivity of 45%.


### SMOTEENN Method:
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTEENN/SMOTEENN_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTEENN/SMOTEEN_confusionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/SMOTEENN/SMOTEEN_classificationreport.JPG)

Using the SMOTEENN method our accuracy score was 62%. Our high risk precision remained at 1% with a sensitivity of 67% and a f1 score of 2%. Our low risk remains at 100% with a sensitivity of 57%.


### RandomForestClassifier Model: 
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/randomforest/RandomForest_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/randomforest/RandomForest_confusionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/randomforest/RandomForest_classificationreport.JPG)

Using the RandomForestClassifier our accuracy score rose to 79%, our high risk precision is up to 4% with a sensitivity of 67% with an f1 score of 7%. Our low risk has changed with a sensitivity at 91% but our precision remaining at 100%. This is due to a lower number of false positives. 


### EasyEnsembleClassifier method:
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/easyensemble/EasyEnsemble_accuracyscore.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/easyensemble/EasyEnsemble_confussionmatrix.JPG)
![](https://github.com/DanMarks12/Credit_Risk_Analysis/blob/main/JPG/easyensemble/EasyEnsemble_classificationreport.JPG)

With the EasyEnsembleClassifier method our accuracy score has climbed to 92.5! Our high risk population has a precision of 7% and a sensitivity of 91% with our highest f1 score of 14%. Our low risk precision remained at 100% with a sensitivity of 94%. 


## Summary
 After looking at the results of all the models we find a lot lacking from all of the results. Some models were good at detecting high risk but most feell short in determining low risk opportunities which would go against the entire purpose of what this analysis sought out to find. We did find more success in thw two ensemble methods: RandomForestClassifier and EasyEnsembleClassifier with much higher accuracy scores and improved sensistivity for high risk population. Alternatively we did see a lot of low risk credits resulting in false positives for high risk which brings me back to loss of opportunities for the bank. If I had to suggest a method to use it would be RandomForestClassifier as we had less false positives than other methods, but in general I would probably suggest we use a differennt method in determining credit score risk as it is a very sensitive fiduciary decision. 
