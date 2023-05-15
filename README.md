#Credit Risk Classification Report

##Purpose

The purpose of this project was to anaylize various techniques by using Logistic Regression Models to identify the best one in which to identify borrowers credit worthiness. The data given was based on past records and was already identified with the "loan_status" column either having a 0 value for healthy or a 1 value for high-risk.

##Stages

The first step was used to create the Logistic Regressions Models was to inport the data from the csv file. 
After the data was imported it was split into features and labels to identify the variable would be anaylzed which in this case was credit worthiness. 
The next step after splitting the data was to further divide it into training and testing sets to analyze.
Two models were used to compare to each other in this process.
The first model was built using the data in a Logistic Regressions Model and training it using the training (X_train, y_train) and testing sets (X_test,y_test) that were generated from the split, fitting the data into the training sets, and then using this data to generate predictions.
The second module was built using the data in a Random Over Sampler Model and training it using the new X_1 and Y_1 variables created and testing sets (X_test, y_test) that were generated from the sp;it, and then using this data to generated new predictions.
Once each model was created it was given an accuracy score, a confusion matrix, and a classification report which could be used to compare the results of each model

##Results

* The Logistic Regression Model had an accuracy score of 95.2% when predictioing on high-risk and healthy loans. When predicting healthy loans the accuracy actually had a precision score of 1.00 and a recall score of 0.99. However, when it was predicting high risk loans it dropped to 0.85 precision score and a 0.91 recall score. With a precision score of 0.85 it means the model is only correctly predicting 85% of the high- risk loans correctly. Furthermore, the model is only identifying 91% of the high risk loans correctly as opposed to the healthy loans in the model getting predicted correctly 100% of the time and being identified correctly 99% of the time.

* The Random Over Sampler Model had an accuracy score of 99.37% when predicting between high-risk and healthy loans.  When predicting healthy loans the accuracy also had a precision score of 1.00 and a recall score of 0.99. However, when it was predicting high risk loans it also dropped to 0.84 precision score and stayed at a 0.99 recall score. With a precision score of 0.84 it means the model is only correctly predicting 84% of the high- risk loans correctly. The model is identifying 99% of the high risk loans correctly which is the same rate as the healthy loans. However, the healthy loans perfect precisions score dwarfs the 84% score the high-risk loans have.

##Summary

Based on the analysis it appears that the Over Sampler Model might be slightly better than Logistic Regression Model one as it has a recall score of 0.99% for both the healthy and high-risk loans, meaning it can more accurately pool them to predict the results. Both models could use improvements on their precisions scores, as while the Logistic Regression Model does more accurately predict the hihg-risk loans it is only 1% better than the Random Over Sampler. If I had to make a recomendation I would recomend the Random Over Sampler Model as the dofference in identifying the high-risk loans correctly of 99% to 91% outweighs the 1% difference in accurately predicting the loans between 84% and 85%. However, I would want to see if we could get a more accurate model on both fronts if possible.
