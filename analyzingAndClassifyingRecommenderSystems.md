<!-- Analyzation and Classification of Recommender Systems (Taxonomy) -->

Learning Objectives for Taxonomy of Recommenders (Lesson Title)
  - To understand the different types of Recommender Systems
    - A framework for analyzing Recommender Systems in general 
    - A specific overview of different recommendation algorithms 
  - To acquire a roadmap for the rest of the course, based on algorithms studied 
  
Model of HOW a Recommender Works: There are 3 Basic Concepts that EVERY Recommender needs 
  * Basic Model 
   ** Users
      - The PEOPLE in our system 
      - The PEOPLE who have preferences for items
      - Users may serve as the SOURCE OF DATA, as in case for Collaborative recommendation 
      - For EACH USER we may have a set of USER ATTRIBUTES (i.e. Demographics) as well as a USER MODEL (i.e. their preference for movie genre)
  ** Items
      - The PRODUCTS/SERVICES/VENDORS that we are choosing to recommend 
      - For EACH ITEM we may have a set of PROPERTIES (i.e. what genre was that movie)
   ** Ratings 
      - The things that EXPRESS OPINION in our system 
      - Where USERS meet ITEMS are in the case of RATINGS 
   ** (Community)
      - More broadly, when we take the users and the items together, we tend to think of having a "COMMUNITY" that expresses a space where all these OPINIONS make sense  
  
1. Analytic Framework - 8 Dimensions of Analysis  
  a. Domain: What's being recommended? What is the content that is being recommended?
    - News, text, articles  
    - Products, vendors, bundles 
    - Matchmaking (recommending people to other people)
    - Sequences (i.e. music playlists) - not just the "set" of songs, but do the "order" of those songs may also matter
    - Interesting property of Domains - the way we treat items that have already been experienced (i.e. music player - we may mostly use music you've heard before, or groceries - that you have already eaten)
      **Examples of Domains for Education and/or Building Community**
        - TripAdvisor - community
        - OWL Learning Tips - education
        - ReferralWeb - expertise finder (education)
    - In some Domains, we are primarily interested in recommending NEW items  
    - Google is a form of Recommender - it is "recommending" websites based on search term 
  b. Purpose: in some cases, the purpose for recommendation is simple - it is an end in itself - We want you to BUY or CONSUME or otherwise take up the recommendation that we give you 
    - In other cases, the recommendations are aggregated as a form of education or a form of building community, and understanding whether recommendations are just come in and consume or are they part of a larger purpose helps us to tailor the recommender for the user's needs 
  c. Recommendation Context: What is the user doing at the time of recommendation? How does that context constrain the Recommender?
    - Depending on what the user is currently doing and who they are with, will affect the level of attention or the degree to which the user will accept an interruption via recommendation
  d. Whose Opinions: Whose opinion is the Recommender based on?
    - Experts, everybody, people like you? - it's usually a mix of all of these
    - Recommender systems, in the broad sense, are based on somebody's opinion, sometimes only yours, but more often other people's opinions as well 
  e. Personalization Level: 
    - Generic/Non-Personalized - NO PERSONALIZATION - everybody gets the same recommendation  
    - Demographic - Could semi-personalize by attaching a recommendation to a certain demographic  
    - Ephemeral - Temporary personalization, by matching to your current activity 
    - Persistent 
  f. Privacy and Trustworthiness: In many cases, people want to know, WHO has to know WHAT about me in order for me to use this Recommender? 
    - How much personal information is needed?
    - Does it have to know the user's identity?
    - Can I use it anonymously?
    - Is there a way I can DENY some of those preferences? - there may be things that were purchased or liked by the user, that they DO NOT want others knowing or associating those purcahses with themselves 
    - Is the Recommender System honest? 
    - How much has the operator "built in" biases? - sometimes these biases are referred to as "Business Rules" 
    - In some cases, the business rules/biases make lots of sense and are consumer friendly 
      - For example, some recommender systems will NOT recommend items that are out of stock 
      - Another example, is a recommender would NOT recommend an item from another store or vendor 
    - Another aspect people are worried about is, vulnerability to a Recommender to external manipulation
    - Transparency of Recommenders - and the degree of which the individuals giving us data have a reputation that will allow us to trust them 
  g. Interfaces
    - What type of output are we getting?
      - Are we getting predictions of specific scores?
      - Are we getting recommendations for specific items? 
      - Are we filtering a search list? 
      - Is our presentation of the recommendation and/or prediction organic or explicit? 
        - Our presentation type will lead into a discussion of different "styles" of interface 
          - Agent: helping the user, critique where you can say "this isn't what I wanted, I was thinking something more along the lines of x"
          - Discussion: search engine or tool
    - What types of input are we receiving?
      - Are you being asked specifically which items you like or how much you like an item on a scale? (Explicit)
      - Are we taking implicit measures to see if you puchased something or how often you return to look at a page? 
  
h. Recommendation Algorithms - There are 4 types of Recommendation Algorithms 
  - Non-Personalized Summary Statistics (and some cases these involve Product Associations)
    - These use External Data from the community
      - Would display recommendations/predictions as lists: Best-seller, Most Popular, Trending Hot 
      - Or display as a Summary of Community Ratings (i.e. Best Liked (Zagat), Highest Rated Restuarant (Zagat)) 
  - Content Based Filtering 
    - Users rate items and from those ratings, we build a model of user preferences against the item attributes (properties, genres, etc.)
      - This means, we can map the PRODUCTS you have RATED (music, movies, etc.) against the ATTRIBUTES of those products (i.e. actor, music genre, etc.)
      - There are also "knowledge-based" Recommender Systems that use the item attributes to form a model of an item space and users navigate interactively to that space 
      - Examples of Content Based Filtering include:
        - Personalized news feeds 
        - Artist or Genre music feeds 
  - Collaborative Filtering (Personalized)
    - This type uses the opinions of others, rathen than attribute data, to predict/recommend 
    - We build on the idea of a user model that is a set of ratings and an item model that is our set of ratings 
    - Using this method, all of our attributes and models can drop off of our diagram (see Lecture Taxonomy of Recommeders @12:00minutes for more details)
    - What we have left is a "Common Core" - a sparse matrix of ratings and our goal is to either: 
        - Fill in those missing values (predict)
        - Select promising cells (cells refer to the "matrix" - see video) that might be ones that we may want to recommend (recommend)
    - Types of Collaborative Filtering Techniques 
      - User-User: 
        - You select a neighborhood of people with similar taste and use their opinions 
      - Item-Item: 
        - You establish relationships among items through the ratings and use those items and your ratings of them to triangulate recommendations 
      - Dimensionality Reduction:
       - You create a lower dimensionality matrix (table) through mathematical techniques that compress the matrix, and then directly find a representation of "taste fit"
    - Notes on Evaluations: When thinking about algorithms, in order to decide with algorithm to use, we'll have to have some way of evaluating them > There are many different types of Evaluations - which the course will cover including:
      - Accuracy of predictions
      - Usefulness of recommendations
        - Correctness
        - Non-obviousness
        - Diversity - being able to deliver a diverse set of recommendations 
        - Computational performance 
      - understanding what you are using a Recommender FOR and how to EVALUATE it properly, will help you to pick the right one 
  - Other Approaches to Recommenders 
    - Interactive recommenders 
      - critique based, or dialog based
    - Hybrids of various techniques 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  