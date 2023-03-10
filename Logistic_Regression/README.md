The Logit Model:
The linear regression techniques discussed so far are used to model the relationship between a quantitative
response variable and one or more explanatory variables. When the response variable is categorical, other
techniques are more suited to the task of classification.
The logit model, or logistic model models the probability, p, that a dichotomous (binary), dependent
variable takes on one of two possible outcomes. It achieves this by setting the natural logarithm of the odds
of the response variable, called the log-odds or logit, as a linear function of the explanatory variables.
Logistic regression is an algorithm that estimates the parameters, or coefficients, of the linear combination
of the logit model. In this worksheet, we will classify a certain binary feature of a dataset using logistic
regression.

A Song of Ice and Fire - GOT Character Dataset:
A Song of Ice and Fire by George RR Martin is a series of epic fantasy novels that is popularly known for its
TV show adaptation, Game of Thrones. The show is well known for its vastly complicated political landscape,
large number of characters, and its frequent character deaths.
The given dataset contains comprehensive information on characters from the book series till the 5th book, A
Dance with Drugons. The data was created by the team at A Song of Ice and Data who scraped it from the
Wiki of Ice and Fire.
This worksheet will focus on using Logistic Regression to predict whether a character in the SolaF world
remains alive by the end of the 5th book, which is captured by the feature actual.


Data Dictionary
actual - Whether the character is alive in the consequent books
(0 if dead, 1 if alive)
name - Name of the character
title - Character's title
male - Gender of the character (1 if male, 0 otherwise)
culture - Culture the character is from
dateofBirth - Character's DoB
mother - Name of the character's mother
father - Name of the character's father
heir - Name of the character's heir
spouse - Name of the character's spouse
book1 - Whether the character appears in Book 1, Game of Thrones
book2 - Whether the character appears in Book 2, A Clash of Kings
book3 - Whether the character appears in Book 3, A Storm of Swords
book4 - Whether the character appears in Book 4, A Feast for Crows
book5 - Whether the character appears in Book 5, A Dance with Dragons
isAliveMother - Whether the character's mother is alive
isAliveFather - Whether the character's father is alive
isAliveHeir - Whether the character's heir is alive
isAliveSpouse - Whether the character's spouse is alive
isMarried - Whether the character is married
isNoble - Whether the character belongs to a noble family
boolDeadRelations - Whether one of the character's relations is dead
numDeadRelations - Count of the character's relations that are dead
isPopular - Whether the character is popular
popularity - Score of the character's popularity


Problems
Problem 1 (1 point)
How many characters from the SoIaF world does this dataset contain information on? Calculate the percentage
of missing data for each column of the dataset and print them out in descending order as a dataframe.
Hint: Make sure to capture data from both missing values in numeric fields and empty strings in descriptive
fields. Convert all missing placeholders to type NA.

Problem 2 (2 points)
Step 1 What are the inferences you can draw from the output dataframe of the previous problem? How
can we handle columns with extremely high proportions of missing data before moving on?
Hint: Does missing data in a column tell you something about the target variable (actual)? If not, set a
missing percentage threshold of 80%, deeming the column as having insufficient data, and drop the column.
Step 2 Impute missing data in the remaining numeric features with a reasonable statistic. Make sure you
observe the distribution of the data in the columns to pick out a reasonable statistic. For categorical variables,
convert the columns to numeric features. Hint: Use the unclass function and impute missing categorical
feature values with a -1.
Bonus
After plotting the age column, do you notice any discrepancies in the graph? What do you think might have
given rise to a such a distribution?

Problem 3 (2 points)
Step 1: Check for Class Bias Ideally, the proportion of both classes of the target variable should be the
same. Is this so in the case of the target variable in this dataset?
Step 2: Create Training and Test Samples Perform undersampling in case of a class bias in the
dataset. Create train and test splits.
Hint: To create the training sample set, sample 70% of the class with lesser rows and sample the same number
from the other class. Use the remaining rows from both classes to create the test split.

Problem 4 (3 points)
Step 1: Build the Logisitic Regression Model Train a logistic regression model to predict whether a
character is dead by Book 5 (feature: actual) using the training split. Use the summary function to print the
beta coefficients, p values and other statistics. Predict characters’ deaths on the test split available.
Step 2: Decide on the Optimal Prediction Probability Cutoff
The default cutoff prediction probability score is 0.5 or the ratio of 1’s and 0’s in the training data. But
sometimes, tuning the probability cutoff can improve the accuracy in both the training and test samples.
Compute the optimal cutoff score (using the test split) that minimizes the misclassification error for the
trained model.
Hint: Use a function from the InformationValue library to perform this task.

Problem 5 (2 points)
Using the optimal cutoff probability, compute and print the following using the predictions on the test set:
1. Misclassification error
2. Confusion Matrix
3. Sensitivity
4. Specificity
Plot the ROC Curve (Receiver Operating Characteristics Curve). What is the area under the curve?
Hint: Use predefined functions for this problem.
