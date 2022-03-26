# Recommendation-Systems
***Building powerful and personalized, recommendation engines with Python***

## What is a recommender systems?
They are systems or techniques that recommend or suggest a particular product, service, or entity.

## Types of recommender systems

 - [Collaborative filtering](https://github.com/Youssef0Eldeeb/Recommendation-Systems#collaborative-filtering)
	 - [User-based filtering](https://github.com/Youssef0Eldeeb/Recommendation-Systems#user-based-filtering)
	 - [Item-based filtering](https://github.com/Youssef0Eldeeb/Recommendation-Systems#item-based-filtering)
 - [Content-based systems](https://github.com/Youssef0Eldeeb/Recommendation-Systems#content-based-systems)
 - [Knowledge-based recommenders](https://github.com/Youssef0Eldeeb/Recommendation-Systems#knowledge-based-recommenders)
 - [Hybrid recommenders](https://github.com/Youssef0Eldeeb/Recommendation-Systems#hybrid-recommenders)

----
----

##  Collaborative filtering
The power of community to provide recommendations.
Ex: *Amazon*

## Collaborative filtering can be classified into two types:
 
 - ## User-based filtering
The main idea is that if we are able to find users that have bought and liked similar items in the past, they are more likely to buy similar items in the future too

> Ex: *Amazon's Customers who bought this item also bought this item too*

- ## Item-based filtering
If a group of people have rated two items similarly, then the two items must be similar. Therefore, if a person likes one particular item, they're likely to be interested in the other item too.

***Collaborative filters suffer from what we call the cold start problem.***

## Content-based systems
Content-based systems do not require data relating to past activity. Instead, they provide recommendations based on a user profile and metadata (like: kind of movie "Romance") it has on particular items.
Ex: *Netflix*
>what Netflix does  is ask you to rate a few movies that you have watched before. Based on this information and the metadata it already has on movies, it creates a watchlist for you.

## Knowledge-based recommenders
The system that asks for certain specifics and preferences and then provides recommendations that satisfy those aforementioned conditions.

> you could ask the user about their requirements for a house, such as its locality, their budget, the number of rooms, and the number of storeys, and so on. Based on this information, you can then recommend properties that will satisfy all of the above conditions.

Knowledge-based recommenders suffer from the problem of low novelty,

## Hybrid recommenders
Hybrid recommenders are robust systems that combine various types of recommender models.
Hybrid systems try to nullify the disadvantage of one model against an advantage of another.
