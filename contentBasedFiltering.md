<!-- Introduction to Content Based Recommenders -->

Learning Objectives 
  - To understand the range and value of content-based approaches to recommendation
    - Pure Information Filtering Systems 
    - Case-based Reasoning Systems 
    - Knowledge-based Navigation Systems 
  - Identify situations in which Content-Based Filtering DOES or DOES NOT work well 
  - Build vector models (matrix - i.e. Excel) representing user preferences and item expression in terms of keywords, tags, or other attributes 
  - Compute recommendations and predictions using the TF-IDF and cosine similarity algorithms 
  - Understand, explain, and apply data normalization in content-based filtering 
  - Understand and be able to explain the TF-IDF algorithm, and in particular, the potential problem that the IDF weighting component is intended to fix 
  - Complete a programming project using the LensKit toolkit, specifically the implementation and customization of tag-based content-based recommendation  

1. ALL Recommender Systems start with "Stable Preferences" 
  - Stable Preferences: these are user preferences that remain CONSTANT 
    Ex: if a user likes blue cotton shirts
  - With Content Based Recommendation, we will use CONTENT ATTRIBUTES as our measure of preference and of stability
  - The KEY ideas:
    - Model items according to relevant attributes 
    - Model or reveal user preferences by attributes 
    - Match both together and you have a Recommender 
    
2. Content-Based Filtering Example: Building a vector (matrix) of attribute or keyword preferences 
  - Krakatoa Chronicle - was a PERSONALIZED newspaper created by a group of students in 1994 and 1995 to illustrate the power of the internet (world wide web) 
    - Next to each article there was a gage, indicating how INTERESTING the USER found that article to be 
    - The amount of space that was taken up by an article and the position of the article in the newspaper was based, IN PART, on HOW INTERESTING you thought the article would be, based on the KEYWORDS you found interesting in previous articles 
    - Also had an EDITORIAL judgement of how important an article was and it would mix this and the USER keyword preferences in an attempt to give you important news slanted towards the news you were interested in seeing 
    - The site would UPDATE any time there was a USER PROFILE change - the WEIGHT for the article was updated depending on what the user changed - which would show how much it matched your keyword 
      - Two Weights: One for user keywords and one for Editor judgement - these would be re-arranged to match score (video @5:50)
      
3. In general, the USER PROFILES can be made in a number of ways 
  - Let users "edit" their profiles from a list of predictions - i.e. what you THINK they like, and then they can fix/edit as needed 
  - We can "infer" a profile from user actions: Reading, click or buy
  - We can "infer" a profile from EXPLICIT RATINGS 
  - We can also merge implicit actions/explicit ratings and create a profile
  
4. How Do We Build Preferences?
  - We start with the idea of "keywords" that users may "like" or "dislike" or have some sort of opinion on 
      Examples: for fashion - keywords: designer, silhoutte, sleeve length, color
  - We could also LEARN keywords that users care about from the population - we could MINE reviews of certain brands, stores, etc
  - We are looking for KEYWORDS that are descriptive of the items, that we can map to the items and that seems related to people's preferences 
  - One of the things we can do is TAKE OUT the keywords that don't work so well (refactor keyword base)
  - From there, we could count the number of times the user chooses the items with those/that keyword, or ignores items with those/that keyword
  
5. How Do We Use preferences We've Gathered?
  - At this point, we could add up the "likes" and "dislikes" 


































    