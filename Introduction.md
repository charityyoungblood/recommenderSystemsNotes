<!-- This file includes an Introduction to Recommender Systems --> 

1. Types of Recommender Technologies 
  - Collaborative Filtering: 
      - Includes building a database of preferences for products by consumers 
      - Uses "neighbors" or other consumers who have historically had similar taste to another customer (i.e. neighbors of Customer1)
      - Products the "neighbors" like, will probably be successful with Customer1
      - Fundamental Challenges for Collaborative Filtering:
        - Improve the scalability of the collaborative filtering algorithms (i.e. instead of using data from tens of thousands of potential neighbors, they need to search tens of millions of potential neighbors)
        - Improve quality of the recommendations for customers (i.e. better customization)