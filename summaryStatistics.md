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
  - Displaying Aggregate Preference (Prediction - here we are predicting a user would like an item, based on showing/displaying aggregate preferences of other users (top lists, most read, etc.))
  
    **Samples of Display Approaches**
      - Show average rating or upvote proportion
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
    
9. Ranking: How do we pick what goes at the top of the list?
  - You DO NOT have to RANK by prediction or the same aggregate preference that you show on the site
  
    - Why NOT rank by score?
      - Too little data (i.e. only ONE 5 star rating for one product and another product which has more reviews, but less stars)
      - Score may be multivariate 
      - Domain or business considerations
        - Item may be old - in terms of news sites, you DO NOT want to display to users the most popular news article from last year - it has to be current  
        - Item is 'unfavored' - for business reasons, you may want to favor some items over others 
  
10. Ranking Considerations 
  - There are a few things to consider when you are computing the rank 
    - Confidence: how confident are you that this item is as good as the score says it is? With lower user averages (i.e. one user who rated 5 stars) - you won't have as much confidence as the product really being excellent vs. if you had 200 people who rated it 5 stars 
    
    - Risk Tolerance: This is going to depend based on the application
      - Is the application one that benefits from high-risk, high-reward recommendation - i.e. there's a chance the user may REALLY love this item, but there is also a high probably they won't like it 
      - Is the application better for a more conservative recommendation - to ONLY recommend something if you are confident that its going to be good 
      
    - Domain and business considerations 
      - Age 
      - System goals: The type of community you are trying to foster on the discussion site 
      
11. Damped Mean
  - One way to deal with some of these issues (specifically in the average context) is to use a damped mean:  
    - When you have few ratings, it is difficult to be confident in the average of those ratings 
    - If there is low confidence due to few ratings, you can assume that, without evidence, EVERYTHING is AVERAGE
    - From there, each rating would serve as a piece of evidence that the particular item is NOT AVERAGE, either it's good or bad 
    - Then when very HIGH or very LOW ratings come in, they can be used as evidence of NON-AVERAGENESS 
    - Using the formula (Week 2: Summary Statistics Part 2 @11:16minutes), we can control the strength of evidence required 
      - To compute the score for an item: 
        - we sum over the users
        - the users ratings for that items
        - we divide by the number of ratings
      - To compute using a damped mean
        - we additionally add the ratings (k) at the global mean - the average of all ratings in the entire system 
        - we add the number of ratings to k - which controls the strength required in order to overcome the global mean
  - Through this process it damps the effect of having just a few extreme ratings early on  
  
12. Statistical Confidence Intervals 
  - Statistical inference provides means of computing confidence intervals of how CONFIDENT you are of the value of the mean or the expected likelihood that someone is going to rate something positively - this interval narrows as you get more and more evidence 
  - Lower bound of statistical confidence interval (i.e. a confidence interval of 95%)
  - The choice of bound affects risk/confidence 
    - If you choose the lower bound you get a very CONSERVATIVE recommendation - you need a lot of evidence to consider something is good and you recommend based on the lower bound of your estimate of how good something is 
    - If you choose the upper bound, you get a recommender that is very willing to take risks on things that might be amazing, but you really don't have enough information yet to tell 
    
13. Domain Consideration: Time 
  - How do we deal with the aspect of time playing a role? (We don't want to show the upvotes for old articles, or items that have short lifetimes (trends))
  - We can use the net upvotes, polynomially decayed by age formula (Summary Statistics Lecture @15:04 minutes) - known as the WILSON SCORE
  
  - ***The WILSON SCORE confidence interval answers the question: Given the ratings I have, there is a 95% chance that the “real” fraction of positive ratings is at least what?***
    - Other Applications of **WILSON SCORE** - The Wilson score confidence interval isn’t just for sorting, of course. It is useful whenever you want to know with confidence what percentage of people took some sort of action. For example, it could be used to:

      - Detect spam/abuse: What percentage of people who see this item will mark it as spam?
      - Create a “best of” list: What percentage of people who see this item will mark it as “best of”?
      - Create a “Most emailed” list: What percentage of people who see this page will click “Email”?

14. Can you predict with sophisticated score (i.e. can we use a damped mean as the aggregate preference that you show)? 
  - YES, but be careful with how you present the rating so as not to create incorrect user expectation
  - Be careful with transparency/scrutiny - if the average rating and damped mean don't match, this could cause problems with presentation
    - If you display an 'average rating' for damped mean, and show ratings, users may be confused 
    - Most important case (low ratings) also easiest to hand verify 
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
      
      
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    