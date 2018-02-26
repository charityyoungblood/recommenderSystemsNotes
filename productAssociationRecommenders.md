<!-- Product Association Recommenders -->

1. As Non-Personalized Recommendations lack "context" - with Product Association Recommenders, we are looking at the very SPECIFIC context of a product or small set of products that a customer is currently looking at or consuming, as an example of a way to constrain what is recommended

2. Product Association Recommenders deal with Ephemeral, Contextual Personalization
  - The products are recommendation based on what you are "currently" shopping for or putting in your cart 
  - Your current navigation is a reflection of your current interest 
  - It is personalized, but NOT personalized to the individual's LONG-TERM tastes and preferences - ONLY personalized to your CURRENT interest 

3. You can take the Product Association Recommendations and turn them into Value Added Comparisons 
  - Amazon does this by comparing 4 products, side by side, displaying their star rating, cost and product descriptions 
  
4. How do we compute Product Association Recommendations? 
  - Manual Cross-Sell Tables
    - Guided by marketing team, they would create tables with products to upsale and cross-sell
    - this is similar to retail - if you have a customer purchasing a product at a given price point, you try to "up-sale" to the same product, but one with more features and a higher price point 
  - Data Mining Associations 
    - We want to make the "manual" process of cross-selling and up-selling, automated
    - People started analyzing transaction data and mining it for associations 
    - The challenge of Data Mining Associations:
      - What are we looking for? 
        - Are we looking for what is most likely to be bought in this context?
        - Are we looking for what is "extra-likely" (or as close to "wthout a doubt") to be bought in this context? 
  - Start with a Simple Formula 
    - percentage of X-buyers who also bought Y, divided by X
    - this formula could be useful, but there may be other variables (i.e. just because people buy ketchup and bananas, doesn't necessarily mean there is a correlation between ketchup and bananas, specifically)
    
  - Bayes' Law: The probability of some event "A", given that "B" also occured can be computed in a number of ways 
    - The probability that "B" occurs, given "A" times the probability of "A" to begin with, divided by the overall probability of "B" 
    - One of the formula's we will use will look at the probability of a customer purchasing a polka dot dress and black pumps
      - The probability of "Y" given "X", how likely is the customer to buy those black pumps ("Y"), given that she just bought the polka dot dress ("X"), versus the probability of "Y" (black pumps) alone, i.e. how likely is it that I'm just buying black pumps 
      - If that ration comes close to 1, then "X" didn't change anything 
      - If I'm 3 times more likely to buy nude shoes after I've bought a polka dot dress, then I am to buy nude shoes without the polka dot dress, then there's a greater probability that it's relevant in this particular context 
      - This may be a better recommendation, then just trying to sell nude pumps 
  - Association Rule Mining - a technique that comes before Recommender Systems started, gave us a "Lift Metric"
    - The "Lift" associated with a pair of products being together is the probability that someone would buy or consume both of them, divided by the product of their individual probabilities (@9:03 in lecture)
    - This is a "Non-Directional Association" - it's not where "X" makes "Y" more likely or "Y" makes "X" more likely, but looks at how they make EACH OTHER more likely 
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    