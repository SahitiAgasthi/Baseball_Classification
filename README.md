# Baseball_Classification

The dataset consists of 18 features and 1340 records. The shape of the dataset is 1340*18. The target column is the Hall_of_Fame which contains three classes 0,1 and 2. We have an imbalanced dataset where majority of records belong to class 0.

Approach taken:
1. Missing values are filled by grouping the 'Position' column and filling the missing values using Mean.
2. Categorical values are converted to numerical values using One-hot encoding.
3. I have stratified the data since we have an imbalanced dataset which has majority of class 0.
4. The Data has been split to Training (75%) and Testing data (25%) and later standardized the data using MinMax scaler.
5. By using Scikit-learn's package, ran different classification models like K-neighbors classifier, Softmax regression, SVM etc.
6. Tuned the parameters using Grid search and 10-fold cross validation.
7. Found that Decision tree classifier gave the highest accuracy of 94%.
8. Checked if Adaboosting, Bagging and Pasting increased the accuracy.
9. Applied PCA on the dataset and reduced the features to 8.
10. Using Keras library, developed Deep learning models with 30 nodes in the input layer, 15 nodes in the hidden layer and 3 nodes in the output layer.
11. I have used Adam and SGD optimizers with categorical_crossentropy losses and Relu, softmax activation functions for the neural network.

# The data description
The data set has 1 file: baseball1.csv.
The baseball1.csv has 18 columns. Target column is the Hall_of_Fame with 3 classes: 0, 1 and 2.
There are 1340 records.

The description of variables is as follows:

Format: variable (type) - description
1. Player (categorical) - name of the player
2. Number_seasons (numerical) - number of seasons played by the player
3. Games_played (numerical) - number of games played by the player
4. At_bats (numerical) - number of At_bats made by the player
5. Runs (numerical) - number of Runs made by the player
6. Hits (numerical) - number of hits made by the player
7. Doubles (numerical) -  number of doubles made by the player
8. Triples (numerical) -  number of triples made by the player
9. Home_runs (numerical) -  number of home_runs made by the player
10. RBIs (numerical) - number of RBIs made by the player
11. Walks (numerical) - number of walks made by the player
12. Strikeouts (numerical) - number of strikeouts made by the player
13. Batting_average (numerical) - batting average= (number of hits) / (number of At-bats)
14. On_base_pct (numerical) - On base percentage (OBP)=(Hits + Walks + Hit by Pitch) / (At Bats + Walks + Hit by Pitch + Sacrifice Flies).
15. Slugging_pct (numerical) - slugging percentage= total bases divided by at bats.
16. Fielding_ave (numerical) - fielding average or fielding Percentage (FPCT) = (put outs + assists) / (put outs + assists + errors).
17. Position (categorical) - Position of players on the field
18. Hall_of_Fame (numerical)(Target variable)- three classes (0,1 and 2)

# Evaluation Metrics
The evaluation metric for this task is Accuracy.
Accuracy is an evaluation metric that allows you to measure the total number of predictions a model gets right. The formula for accuracy is below:
Accuracy = (tn + tp) / (tn + tp + fn + fp).
