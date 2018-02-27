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
    Ex: 
  - With Content Based Recommendation, we will use CONTENT ATTRIBUTES as our measure of preference and of stability
  - The KEY ideas:
    - Model items according to relevant attributes 
    - Model or reveal user preferences by attributes 
    - Match both together and you have a Recommender 
2. Content-Based Filtering Example: Building a vector (matrix) of attribute or keyword preferences 
  - Krakatoa Chronicle - was a PERSONALIZED newspaper created by a group of students in 1994 and 1995 to illustrate the power of the internet (world wide web) 
    - Next to each article there was a gage, indicating how INTERESTING you found that article to be 
    - The amount of space that was taken up by an article and the position of the article in the newspaper was based, IN PART, on HOW INTERESTING you thought the article would be, based on the KEYWORDS you found interesting in previous articles 
    - Also had an editorial judgement of how important an article was and it would mix this and the keyword preferences in an attempt to give you important news slanted towards the news you were interested in 