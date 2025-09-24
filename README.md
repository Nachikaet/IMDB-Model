IMDB-Logistic Regression. In this program, I have used linear regression to predict the outcome of a movie review as positive or negative based on a model trained on previous IMDB reviews.
The dataset is uploaded as a CSV file and is preprocessed using the preprocess command
Then the CountVectorizer module is used to make a sparse matrix of each word in each review and whether they appear or not(called X)
The sparse matrix doesnt take up much memory as it assigns 1 to each present word but doesnt mark non-present ones as '0'
the sentiment column is made into a label column by assigning positive as 1 and negative as 0(called y)
The dataset is then split into testing and training(0.2 and 0.8 respectively) using train_test_split imported from sklearn.model_selection
X and y are then passed through the logistic regression model imported from sklearn and then trained using the training dataset using model.fit
The acuracy is then reviewed using the training split dataset and classification report and confusion matrix are printed along with log loss, brier score and learning curve
The results are as follows:
Accuracy:0.89, recall:0.88, f1 score:0.88
Confusion matrix:
 [[4376  585]
 [ 563 4476]]
Training log loss:0.1356
Test log loss:0.1111
Training brier score:0.0201
Test brier score:0.0127


IMDB- SVM. In this program, I have used SVM to predict the outcome of a movie review based on a dataset containing the reviews and the sentiment as positive or negative
The dataset is uploaded as a CSV file and is preprocessed using the preprocess command
Then the CountVectorizer module is used to make a sparse matrix of each word in each review and whether they appear or not(called X)
The sparse matrix doesnt take up much memory as it assigns 1 to each present word but doesnt mark non-present ones as '0'
the sentiment column is made into a label column by assigning positive as 1 and negative as 0(called y)
The dataset is then split into testing and training(0.2 and 0.8 respectively) using train_test_split imported from sklearn.model_selection
X and y are then passed through the LinearSVM model with 5000 iterations(as it wasn't converging on 1000 iterations) using the training dataset put into model.fit
The acuracy is then reviewed using the training split dataset and classification report and confusion matrix are printed along with log loss, brier score and learning curve
The results are as follows:
Accuracy:0.87, recall: 0.86, f1 score:0.86
Confusion matrix:
[[4271  690]
 [ 657 4382]]
Train Log Loss:0.1556
Test Log Loss:0.3047
Train Brier Score:0.0314
Test Brier Score:0.0927


