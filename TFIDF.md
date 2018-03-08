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

5. Variants and Alternatives 
  - There are a lot of "tweaks" and changes that can be implemented to make TFIDF better in different domains 
  - In certain areas, TF (term frequency) is mostly ignored and turned into a boolean and measured by either the term "appearing" or "not appearing" (this could be displayed as 0 or 1)
    - In this case, we only care about the terms that are "rare" - effectively we have inverse document frequency * occurence 
  - Some applications use variants on TF (term frequency)
  - In cases where TF are LARGE, they are often logorithmically adjusted (i.e. log base 10(tf + 1))
  - In cases where the particular collections of objects or metadata are very WIDELY VARIED in size, you'll often find TF "normalized" - in this case, term frequency would be divided by document length
  - BM25: A ranking function/weighting system that was used by Okapi search engines, which brought a lot of these elements together including term frequency in the document, and how often the term appears in the "query" 
    - Because their queries could have weighted or multiply occuring terms 
    - BM25 also included "document length"  
    - BM25 has a lot of "tweaking constants" in it - depending on how you set them, they "ignore" or "amplify" different factors, which has led to a whole family of BM variants i.e. BM11, BM13 
    
6. "Search" is MUCH Harder
  - This concept in "search" as well as Content Filtering can be MUCH HARDER than simple processing of vectors of terms 
  - Some of the elements that make search hard, are as follows:
    - Phrases and n-grams: sequences of words that happen together 
      Ex: If we were querying the phrase: "computer science", this would not be the same as documents including "computer" and "science"
      - Adjacency: is one factor that is often used with search terms, to see if they are "close to each other" in the query
    - Significance in Documents: 
      - The occurrence of different terms, whether tags or words in a document, may have DIFFERENT SIGNIFICANCE depending on where or how it's applied 
    - General Authority of a Document
      - This also referrs to the Value of a Document or General Rating or prediction score for a movie or other piece of content
      - there are many complex strategies to rate certain documents as "good"
      - Pagerank and similar approaches 
   - Implied Content: what about the cases where the document doesn't have the words, tag, key terms that the article/document is about?
      - One way to find out if a document is relevant when it does NOT have the keyword/tag, is to follow the links on the page or see the page's usage 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
