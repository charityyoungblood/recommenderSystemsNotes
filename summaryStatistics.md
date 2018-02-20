<!-- Summary Statistics: Non-Personalized Recommender Technique -->

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
    