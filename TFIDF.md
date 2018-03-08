<!-- Term Frequency Inverse Document Frequency - this looks at the question of how important or how frequent is this description in the current product, but also how often does it occur across our entire set  --> 

Learning Objectives:
  - To understand the problem that requires a weighting for search or filtering 
  - To understand TFIDF weighting in detail and how it is used in both search and filtering 
  - To understand the range of variants and alternatives to TFIDF 
  - To appreciate the similarities and differences between content filtering and search 
  
1. The Motivation For TFIDF came from primitive searching 
  - If your search term is too vague, you get TOO MANY documents
  - If your search term is too specific, you may not get ENOUGH results 
  - Two factors to consider: 
    - How often does the search term come up in the resulting documents? (websites, pages)
    - Not all terms are EQUALLY RELEVANT - the word "THE" appears in almost every document, but this doesn't necessarily make it the most relevant 
    
2. TFIDF Weighting - this is a strategy of weighting that comes from the field of information retrieval 
  - This stands for Term Frequency * Inverse Document Frequency 
    - Term Frequency: is how often/how many times does the term/tag appear in the document
      - Example: In Movies - you would use "keywords" like actors names, or director names; or "tags" which are words like "suspense", or "car crash", or "New York" 
    - Inverse Document Frequency: how rare is it for a document to have this term(s) or for this movie to have this "tag" across our entire collection 
      - We compute this by the number of documents, divided by the total number of documents with the keyword term or tag
     log(# of documents / # of total documents with term)
    - We multiply these two values together and we get a WEIGHT - that weight is assigned to the particular search term/tag
      - the BIGGER the weight is, the more we factor that in when we're deciding whether we have a match 
     
3. What does TFIDF do? 
  - When applied TFIDF will automatically "demote" common terms and it attempts to promote core terms (a "core term" means it's a ter that is frequently used in the document) over incidental ones
  - TFIDF fails if the core term/concept isn't actually used much, as in the case of your name on a legal document/contract, 
  - TFIDF also fails when people use "poor" search terms (i.e. black for black dress - the keyword "black" will pull up all sorts of items and results that have NOTHING to do with a black dress)
  
4. How does TFIDF Weight Apply to Content-Based Filtering Recommendations?
  - Remember what our goal is with filtering: We want to BUILD a PROFILE of user content preferences and we want to build that profile, most of the time, by taking their implicit or explicit ratings of a set of objects and processing those objects to build this profile 
  - What TFIDF does, as a concept, is create a profile of a document that says "here's an indicator for each keyword, tag or term in the document of HOW IMPORTANT this term IS as a descriptive term for this document"
  - By having that profile of what the content is about, we then have a "weighted vector" that we can fold in to the user profile when we find out if the user "likes" or "dislikes" this particular item
    - Example: If someone liked "Titanic", we would look at the keyword associated with the movie, actor: Leonardo Dicaprio, genre: Romance, etc - and we would MODEL that as a vector, and that vector will be folded in to the user's profile 
    
  
  
  
  
  
  
  
  
  
  
