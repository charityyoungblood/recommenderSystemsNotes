<!-- Summary Statistics: Non-Personalized Recommender Technique -->

Learning Objectives
  - Understand several ways of computing and displaying predictions - in Non-personalized recommenders these take the form of "aggregate preferences"
  - Understand how to rank items with sparse (maybe we don't have a lot of users who have rated an item), time-shifting data (where the relevance of data changes with respect to time)
  - Understand several points in the design space for prediction and recommendation, and some of their tradeoffs 


1. Computing Summary Statistics 
  - What should they mean? i.e. data points
    - Do we want the highest score to be the most popular restaurant?
    - Should it be the average rating? (think about neighborhood hotspots and amount of people who are rating)
    - Should it be the probability that your users would like that restaurant more? 
  - Popularity IS an IMPORTANT metric; there are many cases where what you care about IS popularity 
  - Averages can be MISLEADING 
    - you can adjust the average by summing the percentage of people who like something 
    - you can adjust by normalizing the user ratings (normalization: the process of matching scales; typically this is done by setting the mean to zero and adjusting the standard deviation to make it the same)
  - May want to consider credibility of individual ratings (Ex: imposter reviews on Yelp)

2. Problems with Computing Scores 
  - Self-selection bias: people only score the restaurants they like to go to 
  - Increased diversity of raters: some people don't like certain kinds of food, drinks, etc. 
  
3. Non-personalized popularity statistics or averages can be EFFECTIVE in the RIGHT application
  - We need to understand the relationship between that popularity count or the average and the user need 
  - How much do people agree on what things are good or bad in a particular domain?
  - We need to make sure we pick the right kind of average for the way people rate in that domain 

4. In many cases, it is best to show multiple statistics i.e. a popularity statistic like count, number of sales, average rating and distribution 

5. For ranking, one useful alternative is to average the percentage of ratings that score above or below a threshold
  - the users REALLY liked this item, or the users REALLY hated this item 
  
6. Personalization can address many of the limitations of these non-personalized summary statistics 
    
7. Example
  - Reddit: a widely used, news aggregator site, where the purpose is to provide non-personalized recommendations of news articles to read, based on people upvoting stories that they like 

8. How do we compute the aggregates we show and the ranking that we use for items? 
  - Displaying Aggregate Preference (Different Approaches) 
    - Showing average rating or upvote proportion
      - Pros: Answers the questions "Of people who bothered to express an opinion, do they like it? How much do they like it? How many of them like it?"
      - Cons: It doesn't show popularity (i.e. you may have an average rating of 5 stars, but only one person really liked that item) 
    - Show net upvotes (upvotes - downvotes) or number of likes
      - Pros: Shows popularity
      - Cons: No controversy
    - The percentage of people who have rated the item at least 4 stars (a positive rating)
      - Pros: has a very straightforward interpretation - of the people who rated, how many gave 4 stars or more? 
      - also deals with how different users will deal with ratings scales in different ways, some users may be more likely to rate things high and other tend to rate things lower 
    - A full distribution with a histogram 
      - Pros: Can be complicated, but will give the full picture of ratings 
      - Cons: 
  - ***To consider which display approach to use in a particular site it's useful to think about the GOAL of the display***
    - The PURPOSE of a PREDICTION or of showing aggregate preference, is to help users decide whether they want to buy/read/view the item 
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    