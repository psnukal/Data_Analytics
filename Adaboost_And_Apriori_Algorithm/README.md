This notebook will explore how to implement and utilize AdaBoost
and the Apriori algorithm. For AdaBoost, this notebook utilizes the standard
dataset from sklearn.

Problem 1 (4 points)¶
Fit and evaluate the AdaBoostClassifier from sklearn.ensemble on the wine
dataset. Use the evaluate model to print results.

Problem 2 (3 points)¶
Retrieve the frequent itemsets using the apriori method from mlxtend.frequent_patterns. The code below extracts the basket_sets and
this is provided as input for the apriori method.

Problem 3 (3 points)¶
Now use the association_rules method and pass the frequent_itemsets as
input (achieved using problem 2). Use .head() to display the top five rules.

