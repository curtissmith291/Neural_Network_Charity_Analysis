# Neural_Network_Charity_Analysis

## Overview of the Analysis

The purpose of the analysis was to create a binary classifier using a neural network to predict whether applicants will be successful if provided funding. 


## Results

### Data Preprocessing

- The "IS_SUCCESSFUL" variable is the target for the model. 

- The "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT" were the features for the model. 

- "EIN" and "NAME" were neither targets nor features are were removed from the input data. 

### Compiling, Training, and Evaluating the Model

- Initially, 30 neurons were selected for the first hidden layer and 15 for the second hidden layer; 30 was selected as the input data contained 10 features and 2-3x the number of neurons as the number of inputs is the rule-of-thumb for a first-pass. 

- Prior to any optimization, the model achieved approximately a 73% accuracy on the test data. 

- Multiple steps were taken to try and achieve a higher accuracy:
	
	1) The nodes were increased from 30 to 100 and 15 to 50; this has virtually no effect on the accuracy. The model had a 72% accuracy on the test data. 

	2) A third hidden layer was added; again, the accuracy did not change much. The model had a 72% accuracy on the test data. 

	3) The activation function was changed from "relu" to "tanh"; the model had a 73% accuracy on the test data. 

	4) The binning/bucketing of data was not performed; the model had a 73% accuracy on the test data. 

	5) The bin/bucket size was changed to be more inclusive; the model had a 73% accuracy on the test data. 

	6) Additional columns were dropped. "STATUS" was dropped and the model had a 73% accuracy on the test data. "SPECIAL_CONSIDERATIONS" was dropped and the model had a 73% accuracy on the test data. "ORGANIZATION" was dropped and the model had a 72% accuracy on the test data. 

## Summary

Overall, the results were not terrible, but probably not good enough to rely solely on the model. Use of K-Means could elucidate some additional information on importance of each feature. 