<!-- Demographics and Related Approaches - For "Loosely/Weak Personalized Recommenders" --> 

1. Why use Demographics? - using demographics we can loosely personalize to some attribute(s) of the individual
  - Popularity may not represent the taste of the target user in your application
    - i.e. if the most popular music is for 15 year olds, a 40 year old man may not see that recommendation as valid
  - Demographic attributes (cohorts) include:
    - Age 
    - Gender
    - Race/Ethnicity
    - Socio-Economic Status 
    - Location
  - If I can label users, who we know little about, with certain attributes, can I do a better job making recommendations  for the items they would like by identifying what's popular in THEIR DEMOGRAPHIC?
  
2. How do we use Demographics?
  - We start by identifying available and "most relevant/useful" demographics 
  - Many of the demographic attributes can't be used directly and end up being processed or bucketed 
    - Many of the demographic attributes have to be "sub-divided" into buckets that could provide more relevancy 
      Ex: Age may be grouped by 21-35, 36-45, etc
      Ex: Zipcodes can be transformed into socio-economic status, urban and rural status, dominant ethnicities, etc
      
3. Exploring your data
  - Once you've found relevant demographic attributes to use for your recommendations, it's time to start exploring 
  - At this stage, most people use one of two approaches: 
    - Plot using Scatterplots
      - When scatter plots are similar to a cloud, i.e. NOT in something resembling a tight line, there is a relationship but it's pretty diffuse (not concentrated)
      - If a scatter plot IS similar to a tight line, there is probably a VERY CLOSE relationship 
      - Here you can PLOT different things about the popularity of a product category/product and plot them against demographic attributes (SEPARATELY) and see if you have any potential to do a better job personalizing 
    - Create hypothesis over particular demographic attributes that should relate and they run statistical correlations against these findings 
