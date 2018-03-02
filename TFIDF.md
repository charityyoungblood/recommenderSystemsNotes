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
    - Term Frequency: is how often does the term you're talking about appear in the document
      - Example: In Movies - you would use "keywords" like actors names, or director names; or "tags" which are words like "suspense", or "car crash", or "New York" 
    - Inverse Document Frequency: how rare is it for a document to have this term(s) or for this movie to have this "tag" 
  - We compute this by the number of documents, divided by the total number of documents with the keyword term or tag
      # of documents / # of total documents with term