# CosmicClassifier
###Importing the necessities
We first imported all the libraries and required csv file
###Handling the missing values 
The dataset contained significant missing values across all features, with each column missing between 2,900-3,100 values (nearly half the dataset). Numerical features were handled using median imputation as a robust method to preserve data distribution without being influenced by outliers. For categorical variables like 'Magnetic Field Strength' and 'Radiation Levels', a two-step approach was implemented: first extracting numeric components using regular expressions to standardize formats, then applying mode imputation (filling with the most frequent value) to maintain the original categorical distribution. This comprehensive missing data strategy ensured the dataset's integrity while maximizing usable information for model training.
###Training
Then we trained the model using various methods such as Random Forest, XGBoost, Neural Network, etc. Where we got the highest accuracy in XGBoost as 85.40%. So we exported the model's prediction on test dataset as an csv file such as XGB_Predictions.csv
I have attached all the csv files.
