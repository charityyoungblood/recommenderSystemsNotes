<!-- How Do We Build Content-Based Recommenders, Based on TFIDF Concepts -->

Learning Objectives: (Lecture Title: Content Based Filtering - Deep Dive)

  ## To learn how to build content-based recommenders, based on TFIDF concepts including:
    ## How do we compute vectors to describe items
    ## How do we build profiles of user performance 
    ## How do we predict user interest in items 
    
  ## To understand key variants in implementing CBF recommenders, and their strengths and weaknesses
  
1. Keyword Vector 
  - a "Keyword Vector" starts with the notion that we can define a multi-dimensional "content space", based on the universe of ALL possible keywords 
  - Those keywords may be a "defined vocabulary" - for clothing, we may decided that the things that describe maxi skirts are "flowy", "long", "easy"
    - in this above example, every "flowy", "long", and "easy" keyword/tag is a DIMENSION in the CONTENT SPACE of CLOTHING - EACH KEYWORD has a DIMENSION 
    - Each item has a "position" in that space and that POSITION defines a VECTOR, which is HOW MUCH is this particular skirt "flowy", and HOW MUCH of the skirt is "easy", etc. - each KEYWORD carries a certain WEIGHT
  - Every USER will have a taste profile or MANY taste profiles, that are vectors in that space 
    - Ex: One user may like "flowy" and "easy" maxi skirts that are more on the "flowy" side and less on the "easy" side
  - The MATCH between user preference and items is measured by how closely the two vectors align 
    - In general, we make these vectors the SAME LENGTH - so we are looking at this multi-dimensional angle 
  - In practice, we may NOT want to have an UNLIMITED amount of keywords - we may choose to LIMIT/COLLAPSE the keyword space 
    - Stem: a common technique of NLP (Natural Language Processing) - we'll take words that have different endings, but the same "root" and collapse them together - Ex: "computer", "computing", "compute" would all be ONE keyword 
    - Stop: There are "stop" words or phrases that are so COMMON they have no meaning in telling us anything i.e. "the" or "and" 
    
2. How Do We Represent An Item Through A Keyword Vector?
  - The hard decisions start when you have to represent an "item" as a "keyword vector" 
  - How will we represent an item's relationship to each keyword? 
    ## Is it a simple 0/1 - meaning either the keyword applies or it doesn't?
    ## Is it a simple occurrence count - how many times does this keyword occur?
    ## Should we use something like TFIDF, where we'll count the occurrences times some inverse document frequency term
    ## There are other variants to consider, including: 
      ## How often does the keyword appear in relation to the document length? 
  - By the time we've figured out each keyword, we'll have a vector of "relative strengths" and we'd want to NORMALIZE that vector, so that we could come up with something of unit length to compute with 
  - If a tag is "descriptive" it may be more relevant i.e. "exciting" for movie tag/keyword 
  
3. When talking about features/tags/terms:
  -  We could have a case where each individual tag "t" which is an element of the set of tags "T" is either "applied"  to an item or "not applied"   
    - T sub i could be the "subset" of tags applied to item "i", or we could represent that as a vector "t" sub "i", which is a zero-one vector of whether each tag is "applied" or "not applied"
  - If USERS can apply tags to items, each one and individual time, we could represent "t" sub "ui" as a "tag application" of a particular tag by a user to an item 
  - We also could have cases where tags are "multiply applied" - such as applied by users or by algorithms, in this case, we would make "t" sub "i" a WEIGHTED vector of tags 
    - Example: 
      ## Clothing attributes: if a skirt is BLUE does is matter if BLUE appears in the description 6 times or one time? or size? Do we care about how OFTEN blue appears? 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  