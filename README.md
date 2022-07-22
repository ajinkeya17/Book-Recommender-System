# Book-Recommender-System
Building a Book Recommender system using Collaborative Filtering Approach

## Aim : When a user enters a book name to our final prediction interface then it should output 5 recommendations of books most relevant and closely related to the input book.

## Dataset Used : https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset

## Options for Recommendor Systems : Content based vs Collaborative Filtering based. 

### 1.) Content based
In Content based modelling recommendation is based on similarity between items. A tag is created for each product(movie,book,etc) which describes all it's features relevant for a person's preference towards it (for ex for a movie the tag can be a combo of genre+actors+director+rating). If we know that a user prefers movie A then we can reommend 5 other movies the tags of which have the largest cosine similarity to the tag vector of movie A.

### 2.) Collaborative filtering based
In Collaborative filtering approach we don't recommend based on similarity between items but rather we make recommendations to users based on how other users have rated the content. Collaborative Filtering is a technique or a method to predict a user’s taste and find the items that a user might prefer on the basis of information collected from various other users having similar tastes or preferences. It takes into consideration the basic fact that if person X and person Y have a certain reaction for some items then they might have the same opinion for other items too.

##### Types:

i.) User to User based : In this method we try to find the user who's rating methods are most similar to our target user.
ex: we have 
<br/>
&nbsp;User 1    User 2    User 3 
<br/>
m1   5         2           1
<br/>
m2   3         4           5
<br/>
m3   1         4           4
<br/>
m4   2         1
<br/>
m5   3         5

Now we need to recommend movie to User 3. Based on ratings for m1,m2,m3 User 2 seems to have similar preferences as User 3 and thus we consider that whatever User 2 likes, User 3 will also like. Thus, since from m4 and m5 which User 3 hasn't watched we see that User 2 has liked m5 and thus we recommend m5 to User 3 as well

ii.) Item to Item based : 
In this each item/product is assigned a vector of ratings b different users. The recommendation given to a user who likes one product will be it's n closest product vectors. 

Item to Item based is generally the preferred method and is implemented in our project
