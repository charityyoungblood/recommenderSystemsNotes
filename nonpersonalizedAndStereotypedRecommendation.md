<!-- Non Personalized and StereoTyped Recommendations -->

Learning Objectives for Non-Personalized, Weak and Stereotyped Recommendations
  - Understand the value and drawbacks of non-personalized recommendations
  - Be able to compute nonpersonalized and weakly personalized recommendations using 
    - Aggregated preferences 
    - Product associations 
    - User demographics 

1. Why Do We Want Non-Personalized Recommendations?
  - Effective for NEW USERS; since we don't know a lot about them, we CANNOT provide a PERSONALIZED recommendation
    - However, we still can make recommendations for products, that the new user will find useful and actionable 
  - Nonpersonalized recommendations are very efficient and relatively fast to compute - (i.e. "How many people bought this item") 
  - They can provide a lot of benefit as far as sales, and the user finding the kinds of items they need
  - Non-Personalized recommenders in this case, can provide a very good return on investment 
  - Many applications have been built on common recommended news stories: Reddit, Slashdot, etc
  - There are other applications and media where personalization is near impossible 
  
2. Recommendations have been around long before the digital recommender systems that we know of today (Editorial Recommendations) 
  - Book, movie and music reviews 
  - The New Yorker : "Goings on About Town"
  - Michelin restaurant guides 
  - The Negro Motorist Green Book: recommended places where African-American travelers could stay, eat and get gas in pre-segregation US

3. Print Recommendations that are not based on expert editors (experts in their field)
  - Aggregate Opinion: Zagat Survey - aggregated opinions about restaurants from individual reviewers
    - Produced 30-point aggregate ratings on multiple dimensions
    - Textual review compiled from individual reviewer reports 
    - The Zagat Survey is an example of EXPLICIT feedback (data), where users are providing detailed reviews on food, decor, service and cost 
    - The Billboard Music Chart System, is an example of IMPLICIT feedback (data), where it tracks how many times a song or an album is played on the radio, sold on iTunes
      - The Billboard charts aggregate these kinds of data points in order to produce charts of the currently most popular songs and albums
  - Other Examples of Non-Personalized Recommendations
    - E-commerce ratings and review summaries (i.e. Amazon)
    - Box office charts 
    - "Popular Now" on any news site - most news sites show a "most popular" list 
    
4. Weak Personalization
  - Sometimes we may know a little about the user:
    - Zipcode or location
    - Age, gender, nationality, ethnicity 
    - We can also do a little but of weak personalization depending on what item the user is currently looking at
  - This information can be used for first-pass "STEREOTYPED" personalization
  - Product association allow recommendations based on current page/item/context - we can recommend items that are "comaptible" with the product the user is currently viewing