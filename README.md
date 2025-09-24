IMDB-Logistic Regression. In this program, I have used linear regression to predict the outcome of a movie review as positive or negative based on a model trained on previous IMDB reviews.
The dataset is uploaded as a CSV file and is preprocessed using the preprocess command
Then the CountVectorizer module is used to make a sparse matrix of each word in each review and whether they appear or not(called X)
The sparse matrix doesnt take up much memory as it assigns 1 to each present word but doesnt mark non-present ones as '0'
the sentiment column is made into a label column by assigning positive as 1 and negative as 0(called y)
X and y are then passed through the logistic regression model imported from sklearn and then trained using the training dataset using model.fit
The acuracy is then reviewed using the training split dataset and classification report and confusion matrix are printed along with log loss, brier score and learning curve
