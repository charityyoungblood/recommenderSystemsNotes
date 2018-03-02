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
  - We could also figure out WHICH KEYWORDS are MORE RELEVANT and LESS RELEVANT - what is the weight of sleeve length to designer? will the user care more about the designer or the sleeve length?
  - TFIDF: Term Frequency Inverse Document Frequency - this looks at the question of how important or how frequent is this description in the current product, but also how often does it occur across our entire set
  
6. Case-Based Recommendation
  - The concept of Case-Base Recommendation is we have a database of examples/"cases", i.e. specific products, that we can structure around a set of RELEVANT attributes (i.e. dress color, sleeve length, designer)
  - We can then query and navigate the cases based on examples or attributes and retrieve relevant cases 
  - When we have a "case library" there are a lot of ways we can accomplish this 
  - Example of "Ask Ida" (video @13:10)
  - Case-Based Recommendation would be used in ephermerally-personalized experiences - i.e. what the user is CURRENTLY shopping for/interested in 
  - These are also much easier to explain to a user (i.e. selecting "this" over "that")
  
  - Challenges and Drawbacks to Content-Based Techniques 
    - They depend on well-structured attributes that align with preferences (this is hard to use for something with an "emotional" connection, how the product makes the user feel, as in selecting attributes/keywords that describe their taste in art or music)
    - They depend on having a reasonable distribution of attributes across items and vice versa (i.e. if all the items are almost identical, in terms of attributes - this technique would not be useful)
    - Content-Based Recommendations are also LESS LIKELY to find SURPRISING recommendations/connections (i.e. chilli pepper oil with pecans)
    - It is also harder to find COMPLEMENTS or items that COMPLEMENT an item, than it is to find substitutes (this is not as hard to do with fashion - as we generally know what will complement a look)
  
7. Knowledge-Based Recommender 
  - If we have a library of examples ("cases") we can navigate from item to item without having to ask the user a survey of questions 
  - Example of this is FindMe Systems (i.e. Entree at video 16:46)
  
8. Take Aways
  - There are MANY ways to recommend based on content using product attributes 
    - Long Term Recommendations: can be implemented by building profiles of content preferences (via the use of keywords)
    - Short Term Recommendations: can be implemented by building a database of cases (items) and navigating through those cases 
  - Content-Based techniques work without a large set of users (but you will need item data)
  - Content Based Recommeders are good at finding SUBSTITUTES 
  - " " good at helping users navigate through items to purchase 
  - " " are easy to explain to users 


































    