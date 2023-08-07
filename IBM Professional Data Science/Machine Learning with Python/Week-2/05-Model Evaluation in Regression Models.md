The goal of regression is to build a model to accurately predict an unknown case. 
The three major types of evaluation approaches that can be used to achieve this goal are:
# 1. Train and Test on the Same Dataset:
You train the model on the entire dataset, then you test it using a portion of the same dataset. 
	CONS:
	This evaluation most likely has a High Training Accuracy and Low out-of-sample accuracy since the model knows all of the testing data points from the training.

![Train And Test](06-Train-Test_on_Same_Dataset.png)

# 2. Train/Test Split. 
We select a portion of our dataset for training (eg:row zero to five), and the rest is used for testing (eg: row six to nine). 
The model is built on the training set then, the test feature set is passed to the model for prediction. Finally, the predicted values for the test set are compared with the actual values of the testing set.
	PROS: This will provide a more accurate evaluation on out-of-sample accuracy since the testing dataset is not part of the dataset that has been used to train the data.
	CONS: It's highly dependent on the datasets on which the data was trained and tested

![Train And Test](07-Train-Test_Split.png)

# 3. K-Fold Cross-Validation: (multiple train/test splits)
We use the first 25 percent of the dataset for testing and the rest for training. The model is built using the training set and is evaluated using the test set. Then, in the next round or in the second fold, the second 25 percent of the dataset is used for testing and the rest for training the model. Again, the accuracy of the model is calculated. We continue for all folds. Finally, the result of all four evaluations are averaged. In this model no training data in one fold is used in another.

![Train And Test](08-K-Fold_Coss-Validation.png)


# The 2 Types of Model Accuracy are:
## 1. Training Accuracy:
Training accuracy is the percentage of correct predictions that the model makes when using the test dataset. Having a high training accuracy may result in an over-fit the data. This means that the model is overly trained to the dataset, which may capture noise and produce a non-generalized model.

## 2. Out-of-Sample Accuracy:
Out-of-sample accuracy is the percentage of correct predictions that the model makes on data that the model has not been trained on.
