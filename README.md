Data Preprocessing and Model Training Summary
1. Importing the Necessary Libraries and Dataset
The first step involved importing all the essential Python libraries required for data analysis, preprocessing, and model training. This included libraries such as pandas, numpy, and matplotlib for data manipulation and visualization, as well as scikit-learn, XGBoost, and TensorFlow/Keras for machine learning and deep learning model implementation. Additionally, we loaded the dataset from the provided CSV file to begin the preprocessing phase.

2. Handling Missing Values
The dataset exhibited a significant proportion of missing values across all features, with each column missing approximately 2,900–3,100 values, which accounted for nearly half the dataset. To address this issue effectively, different imputation techniques were applied based on the feature type:

Numerical Features: Missing values were handled using median imputation, as it is a robust method that preserves the original data distribution while mitigating the impact of outliers. The median was chosen over the mean to avoid skewing the data due to extreme values.

Categorical Features: Features such as ‘Magnetic Field Strength’ and ‘Radiation Levels’ contained categorical values with mixed formats. A two-step approach was implemented to handle these variables:

First, we used regular expressions to extract and standardize the numeric components embedded within categorical labels, ensuring uniformity in data representation.

Next, we applied mode imputation, filling missing values with the most frequent category to preserve the original categorical distribution and prevent data imbalance.

This comprehensive approach to handling missing data ensured the dataset’s integrity, prevented bias, and maximized the amount of usable information for training machine learning models.

3. Model Training and Evaluation
Once the dataset was preprocessed and cleaned, we proceeded with training machine learning models to classify planets into 10 different categories. A diverse set of models was employed to compare their effectiveness:

Random Forest: A powerful ensemble learning method that combines multiple decision trees to improve accuracy and reduce overfitting.

XGBoost: A gradient boosting algorithm known for its efficiency and high predictive performance, particularly on structured data.

Neural Networks (Deep Learning): A multi-layer perceptron (MLP) model built using TensorFlow/Keras to capture complex patterns and nonlinear relationships in the data.

After evaluating the performance of these models, XGBoost achieved the highest classification accuracy of 85.40%, outperforming other methods. Given its superior performance, we finalized the XGBoost model for predictions.

4. Exporting Predictions
The trained XGBoost model was then used to generate predictions on the test dataset. The predicted classifications were exported as a CSV file named "XGB_Predictions.csv", ensuring reproducibility and easy integration for further analysis or deployment. All relevant CSV files containing processed data and predictions were saved and attached for reference.
