# Satyam-Sinha_Datahack
Here's a concise summary of the approach for first model using Logistic Regression:

To tackle the problem, I started by loading the training features, training labels, test features, and the submission format data from their respective CSV files. I then merged the training features and labels on `respondent_id` and dropped the `respondent_id` column from both the training and test datasets, as it is not a feature needed for the model.

Next, I identified the features and target variables (`xyz_vaccine` and `seasonal_vaccine`). I used a column transformer to preprocess the data: for numerical features, I used a median imputer, and for categorical features, I applied a most frequent imputer followed by one-hot encoding.

I created a pipeline with this preprocessing step and a logistic regression model. I trained this model separately for `xyz_vaccine` and `seasonal_vaccine`. After training, I used the models to predict the probabilities of vaccination for the test set.

Finally, I prepared the submission file by filling it with these predicted probabilities and saved it as `output_LogisticRegression.csv`.

Here's a concise summary of the approach for the second model using RandomForestClassifier:

I did everything same as earlier, but I used RandomForestClassifier model.

I trained this model separately for the `xyz_vaccine` and `seasonal_vaccine` target variables. After training, I predicted the probabilities of vaccination for the test set.

Finally, I prepared the submission file by including these predicted probabilities and saved it as `output_RandomForest.csv`.
