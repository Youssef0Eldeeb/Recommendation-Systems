
<br />
<div align="center">
  <h2 align="center">Recommendation-Systems</h2>
   <p align="center">
    <h4 align="center">Building powerful and personalized, recommendation engines with Python</h4>
    <br />
      </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#Getting Started with Recommender Systems">Getting Started with Recommender Systems</a>
      <ul>
        <li><a href="#What is a recommender system?">What is a recommender system?</a></li>
        <li><a href="#Types of recommender systems">Types of recommender systems</a></li>
        <ul>
        <li><a href="#Collaborative filtering">Collaborative filtering</a></li>
         <ul>
        <li><a href="#User-based filtering">User-based filtering</a></li>
        <li><a href="#Item-based filtering">Item-based filtering</a></li>
      </ul>
        <li><a href="#Content-based systems">Content-based systems</a></li>
        <li><a href="#Knowledge-based recommenders">Knowledge-based recommenders</a></li>
        <li><a href="#Hybrid recommenders">Hybrid recommenders</a></li>
      </ul>
      </ul>
    </li>
    <li>
      <a href="#Manipulating Data with the Pandas Library">Manipulating Data with the Pandas Library</a>
    </li>
    <li><a href="#Building The first recommender">Building The first recommender</a></li>
    <ul>
        <li><a href="#The simple recommender">The simple recommender</a></li>
        <li><a href="#The knowledge-based recommender">The knowledge-based recommender</a></li>
      </ul>
    <li><a href="#Building Content-Based Recommenders">Building Content-Based Recommenders</a></li>
    <ul>
        <li><a href="#Plot description-based recommender">Plot description-based recommender</a></li>
        <li><a href="#Metadata-based recommender">Metadata-based recommender</a></li>
      </ul>
    <li><a href="#Getting Started with Data Mining Techniques">Getting Started with Data Mining Techniques</a></li>
    <ul>
        <li><a href="#"></a></li>
        <li><a href="#"></a></li>
      </ul>
    <li><a href="#Building Collaborative Filters">Building Collaborative Filters</a></li>
     <li><a href="#Hybrid Recommenders">Hybrid Recommenders</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#References">References</a></li>
  </ol>
</details>

# 1. Getting Started with Recommender Systems
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

  Collaborative filtering can be classified into two types:
   - ## User-based filtering


   
The main idea is that if we are able to find users that have bought and liked similar items in the past, they are more likely to buy similar items in the future too

> Ex: *Amazon's Customers who bought this item also bought this item too*

<img width="800" alt="Customers who bought this item also bought" src="https://user-images.githubusercontent.com/55714593/160233374-ac209a55-b9ad-4a70-85d0-11ec78d8ba91.png">
<img width="800" alt="Customers who searched for this item ultimately bought" src="https://user-images.githubusercontent.com/55714593/160233812-4041c564-334c-4c11-a8c4-fa8dcb97c5c8.png">


- ## Item-based filtering
If a group of people have rated two items similarly, then the two items must be similar. Therefore, if a person likes one particular item, they're likely to be interested in the other item too.

<img width="800" alt="Products related to this item" src="https://user-images.githubusercontent.com/55714593/160233622-dd584e49-dd3d-4daf-becf-58bc6d790d00.png">

***Collaborative filters suffer from what we call the cold start problem.***

## Content-based systems
Content-based systems do not require data relating to past activity. Instead, they provide recommendations based on a user profile and metadata (like: kind of movie "Romance") it has on particular items.
Ex: *Netflix*
>what Netflix does  is ask you to rate a few movies that you have watched before. Based on this information and the metadata it already has on movies, it creates a watchlist for you.

## Knowledge-based recommenders
The system that asks for certain specifics and preferences and then provides recommendations that satisfy those aforementioned conditions.

> you could ask the user about their requirements for a house, such as its locality, their budget, the number of rooms, and the number of storeys, and so on. Based on this information, you can then recommend properties that will satisfy all of the above conditions.

Knowledge-based recommenders suffer from the problem of low novelty

## Hybrid recommenders
Hybrid recommenders are robust systems that combine various types of recommender models.
Hybrid systems try to nullify the disadvantage of one model against an advantage of another.

# 3. Building The first recommender
- ## The simple recommender
**The steps that used in this recommender are as follows:**
			1. Choose a metric (or score) to rate the movies on  
			2. Decide on the prerequisites for the movie to be featured on the chart 
			3.  Calculate the score for every movie that satisfies the conditions  
			4. Output the list of movies in decreasing order of their scores
			
 ***The dataset you can download it [from here](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)***

- ## The knowledge-based recommender
We are going to go ahead and build a knowledge-based recommender on top of our IMDB Top 250 clone. This will be a simple function that will perform the following tasks:
1.  Ask the user for the genres of movies he/she is looking for
2.  Ask the user for the duration
3.  Ask the user for the timeline of the movies recommended
4.  Using the information collected, recommend movies to the user that have a high weighted rating (according to the IMDB formula) and that satisfy the preceding conditions

# 4. Building Content-Based Recommenders
**We are going to build two types of content-based recommender with our movies dataset**
We use some feature extraction techniques like:
 - CountVectorizer. you can know more. [from here](https://www.geeksforgeeks.org/using-countvectorizer-to-extracting-features-from-text/)
 - TF-IDFVectorizer.  you can know more. [from here](https://www.geeksforgeeks.org/understanding-tf-idf-term-frequency-inverse-document-frequency/)
 
Also, you can know more about **The cosine similarity score**. [from here](https://www.sciencedirect.com/topics/computer-science/cosine-similarity)
 - ## Plot description-based recommender
    This model compares the descriptions and taglines of different movies, and provides recommendations that have the most similar plot descriptions
 - ## Metadata-based recommender
	This model takes a host of features, such as genres, keywords, cast, and crew, into consideration and provides recommendations that are the most similar with respect to the aforementioned features.


