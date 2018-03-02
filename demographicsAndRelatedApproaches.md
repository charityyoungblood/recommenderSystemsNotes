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
    
4. Break down Summary Statistics by Demographic 
  - After you've found relevant demographic attributes and explored the data, breaking down your summary statistics by demographics is the next step 
    Ex: on your website, you can show the most popular products for men (when your site visitors are male) and popular products for women (when your site visitors are female)
  - Can use multiple demographic attributes to personalize the product recommendations 
    Ex: male age 18-25 display one product, and male 40-50 a different product (Factorial recommendation)
  - If you have multiple relevant demographic attributes, you may want to consider a MULTIPLE REGRESSION MODEL
    - this would be a model that predicts item preference/item sales or some other measure of popularity, based on the demographic statistics 
    - MULTIPLE REGRESSION MODELS tend to need a lot of data to be utilized, but they provide nice predictive models 
    - If you chose this model type, you need to make sure you have the model "fit" the kind of data you have  
      - Linear Regression: if you have MULTI-VALUE data like RATINGS or measures of popularity that go beyond "purchased item" and "did not purchase item" you may want to use linear regression to build a linear combination of demographics that predicts those multiple values 
      -  : if your data is primarily 0/1 data or "like", "didn't like" or purchase data (i.e. purchase, didn't purchase), then you'll want to use LOGISTIC REGRESSION that attempts to predict the probability of something being a 1, given the input demographic attribute(s)
      
5. Important Points When Using Demographics
  - You do need to deal with the possibility of UNKNOWN DEMOGRAPHICS 
    - There is NO data set where you will have perfect demographics 
    - You can model unknown demographics in a number of ways: 
      - Overall Preference
      - Expected demographics for people who are new to the community and that you know little about (i.e. your loyal customers who you know a lot about and a new comer comes along, who fits the demographics of your loyal customers, and you can assume they will have similar LIKES and DISLIKES as your loyal customers)
      - Demographics DO NOT have to be PERSONAL DATA - they could reference how long a person has been using your site 
      - You can also model the UNKNOWN DEMOGRAPHICS separate from the other users until you can learn more about their tastes and preferences 
  - If getting demographics is useful, one of your KEY STEPS is getting data on users, which can be collected from various sources including advertising networks, loyalty clubs, surveys, etc. 
  - In some cases, people have successfully predicted demographics from data (i.e. Facebook data - due to the amount of public disclosure that occurs on Facebook, in postings, etc, it's relativey easy to predict certain things from that Facebook data, including demographic data and psychographic data (personality indicators, and information about someone's psyche)
  
6. Limits and Power of Demographics 
  - Part of the reason that demographics work so well, in most cases, is products and content is created with a particular audience in mind (target market)
    - This includes television shows, magazines, personal products, etc where advertisements are sold
    - Traditionally, Advertisers drive content so that that content could be used to pitch advertisements for products and generate sales 
  - Demographics can FAIL MISERABLY for people's who tastes DO NOT match their demographics 
    Ex: someone who doesn't listen to the type of music their peers listen 
  - Demographics also FAIL when the product is CROSS CUTTING - some products need to appeal very broadly, and if they are NOT TARGETED they cannot be used (i.e. paper, pens)
  - Demographics will NEVER be a perfect solution, but they can be a VALUABLE and effective solution, depending on the product and application 
      
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
