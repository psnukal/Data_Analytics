Collaborative & Content based filtering:
The Collaborative filtering method for recommender systems is a method
that is solely based on the past interactions that have been recorded between
users and items, in order to produce new recommendations.
The Content-based approach uses additional information about users and/or
items. The Content-based approach requires a good amount of information
about items’ features, rather than using the user’s interactions and feedback.

Task:
After the disastrous pitfall of Game of Thrones season 8), George R. R. Martin
set out to fix mindless mistakes caused by the producers David and Daniel.
A few years down the line, we now are witnessing George R. R. Martin’s latest
work: House of the Dragon. This series is a story of the Targaryen civil war
that took place about 200 years before events portrayed in Game of Thrones.
In this notebook you will be exploring and analying tweets related to The House
of Dragon TV series. First we shall tokenize the textual data using TF-IDF.
Then we will proceed to find the tok-k most similar tweets using cosine similarity
between the transformed vectors.
The dataset has been extracted using the Twitter API by utilizing a specific
search query. The data has been extensively preprocessed and a small subset
has been stored within the twitter_HOTD_DA_WORKSHEET4A.csv

Note: This notebook may contain spoilers to the show.

Data Dictionary:
author_id: A unique identifier assigned to the twitter user.
tweet_id: A unique identifier assigned to the tweet.
text: The text associated with the tweet.
retweet_count: The number of retweets for this particular tweet.
reply_count: The number of replies for this particular tweet.
like_count: The number of likes for this particular tweet.
quote_count: The number of quotes for this particular tweet.
tokens: List of word tokens extracted from text.
hashtags: List of hashtags extracted from text.

Problem 1 (4 points)¶
Tokenize the string representations provided in the tokens column of the
DataFrame using TF-IDF from sklearn. Then print out the TF-IDF of the first
row of the DataFrame.

Problem 2 (4 points)¶
Find the top-5 most similar tweets to the tweet with index 7558 using cosine
similarity between the TF-IDF vectors.

Problem 3 (2 point)¶
A great disadvantage in using TF-IDF is that it can not capture semantics. If
you had classify tweets into positive/negative, what technique would you use to
map words to vectors? In short words, provide the sequence of solution steps
to solve this task. Note: Assume sentiment labels have been provided.
