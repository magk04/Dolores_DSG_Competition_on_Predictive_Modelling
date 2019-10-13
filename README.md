# Dolores_DSG_Competition_on_Predictive_Modelling
A Repository having code for the Dolores(i.e. a predictive modelling competition organised by DSG IITR)

# 1. Problem Statement
Make it about machine learning – that seems to be a theme behind Google’s return to robotics, an effort that reportedly has more to do with software than creating mechanical creatures that resemble human beings. Nowadays companies are synthetically generating more and more datasets from the realistic simulation of the dynamics of robots. Your task is to predict the angular acceleration (target) of one of the robot arm's links. The training dataset contains features like angular positions, velocities and torques of the robot arm.

# 2. Evaluation Criteria
The evaluation metric is RMSE(Root Mean Squared Error).

# 3. Model Used
The Random Forest Regressor is used along with some feature mean normalisations as some overfitting is avoided in Random Forest Regressor due to more number of trees as compared to other form of modelling.

# 4. Imports Required
Following Imports were made to make the predictions :
• Imported Numpy as np for the Linear Algebra operations.
• Imported Pandas as pd for the data processing operations.
• Imported matplotlib.pyplot as plt for Plotting certain plots for visualisation.
• Imported train_test_split and mean_squared_error from sklearn for cross validation.
• Imported RandomForestRegressor from sklearn for regression of the model.

# 5. Coding Summary
Python3 in Notebook was used to code the predictive model as follows :
• Two data frames df and df1 were formed storing train and test data respectively.
• Mean normalisation was done on some features such as tau1, tau2, tau3 etc.
• Visualisations and Inferences were drawn by plotting several plots using matplotlib.
• Unwanted set columns (‘target’, ‘id’ and ‘Unnamed: 0’ ) and ( ‘id’ and ‘Unnamed: 0’ ) were dropped from data frames df and df1 respectively.
• Training data was split in train and test samples as the fraction of test size as 0.3 and random state as 42.
• Shapes of x_train and y_train were checked and found to be same.
• Random forest Regressor was applied on the train data and used to predict test data splitted from the training data.
• The root mean square error was then calculated and which was found to be around 0.52.
• The model was then used to predict the test data provided.
• Submission Data Frame was then made having the features same as in the sample_submission.csv file.
• The final csv file was then submitted in the competition.

# 6. Mean Normalisation
Mean normalization was done to change the values of some columns such as tau1, tau2 etc. in the dataset to use a common scale around -2 to +2, without distorting differences in the ranges of values or losing information.

# 7. Cross-Validation
Cross Validation is a technique in which the train data is splitted into temporary training and test data which is used to cross validate the model before directly submitting the model. Here I split the 30% of training data as test data and remaining as train data. Then the model is trained in this temporary splitted train data and tested on that temporary test data. Then root mean square error was calculated comparing the predicted value of target with original value of test data.

# 8. Submission
The model was then used to predict the test data provided. Submission Data Frame was then made having the features same as in the sample_submission.csv file. The final csv file was then submitted in the competition.
