# Joke_Recommendation_System
Implementing a Jokes Recommender Engine using Jokes dataset

In this project, we have implemented a joke recommendation system. We have used 73,421 users rated jokes dataset provided by Jester Research project under flagship of UC Berkeley Laboratory for Automation Science and Engineering to find correlations between users and jokes by learning from the previous viewing history of users and to provide recommendations for jokes which users would prefer to see most. We firstly implemented a neighborhood-based user user Collaborative Filtering method which was intuitive and based on like people rate alike. Secondly, we used a Content Filtering method where we used topic modeling approach to create the topics of the 100 jokes!!


# Dataset Description:
We have dataset of 100 jokes and 73,421 user ratings of these 100 jokes
provided by Jester Research
project under the flagship of UC Berkeley Laboratory for Automation
Science and Engineering.
The data contains 100 html files of jokes and 3 csv data of user ratings.
Here is the link to the dataset. (http://eigentaste.berkeley.edu/dataset/)


# Neighborhood based Collaborative filtering:
Collaborative Filtering techniques make recommendations for a user based
on ratings and preferences data of many users.User-user collaborative
filtering approach relies on the idea that users who have similar rating
behaviors so far, share the same tastes and will likely exhibit similar rating
behaviors going forward.The algorithm first computes the similarity
between users by considering ratings both users have in common. The
similarity is computed by using the Pearson Correlation.


# Content based Filtering:
Content based filtering system doesn't involve other user's likes or dislikes
but one's own likes or dislikes.The algorithm will simply pick items with
similar contents to recommend to a user based on the user's
rating to other products.
We have first clustered 100 jokes into 10 clusters using topic modeling
technique with LDA since joke metadata wasn't available so we had to
create one. Once the joke group is determined, we selected an active user
and recommended a joke for him based on his highest rating.


# Hybrid:
Hybrid recommendation system combines both content based and
collaborative filtering to address their limitations and improve their
performance. In this technique, we find the mean ratings using both
methods for all the unrated jokes for a user. It then recommends the joke
with the highest mean rating to the user.
