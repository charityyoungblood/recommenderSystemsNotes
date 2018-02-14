<!--What is the Output of a Recommender System?--> 

Learning Objectives for Predictions and Recommendations (Lesson Title)
  - To understand the ways in which Recommender output can be used 
  - To understand the distinction between predictions and recommendations 
  - To understand the distinction between organic and explicit presentation 
  - To review examples and understand which presentation makes most sense in different applications 
  
1. Predictions
  - In many Recommender Systems, what is being computed, is an estimate of how much you will like an item, how likely you are to purchase an item, or some other numeric score that is supposed to correlate with your opinion of an item
  - If a prediction is wrong, WAY OFF, i.e. it predicted you would like yellow sneakers, and you HATE yellow sneakers, than you are more likely to distrust future and other predictions from the Recommender system 
  
2. Recommendations
  - Recommendations DO NOT make the bold statement that predictions do
  - Recommendations are SUGGESTIONS of things you MIGHT like, things that "fit" what you're doing right now
  - Recommendations are displayed in "lists", i.e. "Top 5" or "Top 10" 
  - Recommendations can also be displayed to the user by item (without the list)
  
3. What are the pro's and cons of Predictions vs. Recommendations?
  - Often the two come together
  - Predictions
    - Pro: they can help quantify item - it gives you a very clear understanding on some scale how "good" something is
    - Con: they can provide something falsifiable - it gives you something that can be WRONG (this is a real DOWNSIDE to predictions)
  - Recommendations
    - Pro: they provide good choices as a default 
    - Con: if perceived as top-n, this can result in failure to explore (if top few seem poor) - meaning if the recommendations are listed from best to worst, once they look at a few of the "worst" they'll stop looking 
    
4. How Explicit is the prediction or recommendation (vs. organic)?
  - Explicit: refers to the image of the "pushy" salesman - before knowing ANYTHING about the customer, the explicit prediction will predict a product for you to purchase or one it ASSUMES you will like "Here's something we picked just for you! It's 4.5 stars"
    - The explicit recommendation or prediction did create "awareness" of the product(s), which can be a good thing
    - The drawback of this approach, is people feel uneasy when someone recommends or predicts something, with little information about the customer themselves 
    - Another drawback, is customers start to question your motives, feel taken advantage of and do not TRUST the recommender (i.e. the PUSHY salesman)
  - Organic: refers to the "subtle" salesman - placing products that you MAY like in a viewable part of the store, or  "strategically" placed online for you to see 
  - The proper technique for creating a Recommender System is a healthy balance of BOTH explicit and organic recommendations and predictions 
  
  
