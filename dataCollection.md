<!-- Where does the data that drives Recommender Systems, come from? How is it collected? -->  

Learning Objectives for Preferences and Ratings (Lesson Title)
  - Understand what data Recommenders can use to learn what users like 
  - Identify types of data collected from users 
  - Understand when different data types are possible and appropriate 
  - Be able to identify types of preference data likely used in a system 


1. In order to do recommendation of ANY form, you need to have data about what items users are likely like, or what items go together 

2. Though there are exceptions, many systems collect this data from their users 

3. When collecting data, it is important to know WHAT you are trying to learn > With Recommender systems, we are trying to learn PREFERENCE - we want to learn, WHAT users like 
  - PREFERENCE is used broadly 
  - Users display their PREFERENCES in a number of ways. Theses ways can be split into two categories 
    - Explicit Data: where the user is taking an action for the purpose of telling either the system or other users of the system what they think about a particular item 
      - Rating
        - One of the most common Rating interfaces is "Star Ratings" 
        - Several design decisions (i.e. How many stars do you use? Do you use 1/2 stars)
        - Research has shown the "1/2" stars don't give us any additional benefit, when it comes to analyzing that data
        - Another Rating interface is "Up or Down" votes, or "Like or Not Like"
        - "Up or Down" votes are common with short-lived items, or items that DO NOT have a long life span 
        - "Up and Down" votes are very low cost to rate - the user only decides if they like the item/article or not, instead of having to process (think about) how many stars to give 
      - Review
      - Vote
      - Other Interfaces (Occassionaly Used) to collect Preference Data:
        - Continuous Scales: constrain users very little > these enable users to rate anywhere on a fairly wide ranging scale 
        - Pairwise preference: these ask users to judge whether they like one item better than another, rather than just rate one item on an absolute scale  
        - Hybrid
        - Temporary
    - Implicit Data: the user is NOT telling anything, but through their actions we can determine what they think about a particular item 
      - Click 
      - Purchase 
      - Follow 
        - Early implicit data included time as a variable for preference; i.e. the longer the user spent reading or listening to the product, the more likely it was that they liked that item - this correlated reasonably well with the user rating of the article/song/product
          - In Music, IMMS (Intelligent Music Management System) - is a plugin for audio players that tracks your listening 
          - If you listen through a song all the way, IMMS records that, also if you skip a song, IMMS records that 
    - Binary Actions 
      - Clicking on link
      - NOT clicking on a link 
      - Purchase 
      - Follow/Friend 
      
4. When are ratings provided? - Particularly, when are the ratings provided in relation with when the user consumed the item
  - Consumption ratings are provided during or after immediately experience an item (i.e. when you watch a Youtube video and you rate the video RIGHT AFTER you view it)
  - Memory ratings are provided some time after the user experiences the item 
  - Expectation ratings - the user has not experienced the item, this rating is based on what the user "expects" to get out of the item > Expectation ratings are usually used with high-cost items (i.e. house, car, etc)
  - Joke ratings: usually provided on absurd or ridiculously high priced items or items of cultural significance (i.e. star memorabilia)
  
5. Difficulties with Ratings 
  - Noise
  - Preferences can change
  - Different users 
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      