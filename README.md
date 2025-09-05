# Contents of the repository:
This repository contains the following files:
 - Notebook.ipynb
 - The datasets folder, containing `advice_posts_def.csv` and `advice_comments_def.csv`
 - Report


## Notebook
The notebook compares **BM25** (a lexical retrieval model) and a **bi-encoder** (dense semantic retriever) for ranking answers to advice-seeking queries. Evaluation is performed using standard information retrieval metrics on a Reddit-style comment dataset.
### Structure of the Notebook

###  Reddit Dataset Construction

-   Creation of posts and comments dataset
    
-   Loading posts and comments dataset
    
-   Creation of qrels dataset via Wilson score and quantile-based relevance levels
    

###  Exploratory Data Analysis

-   Distribution of post lengths (in words) for Title and Description
    
-   Distribution of comment lengths (in words)
    
-   Top word frequency in posts (excluding stop words) for Title and Description
    
-   Top word frequency in comments (excluding stop words)
    
-   Correlation Matrix: Comment features vs. Relevance level
    

###  Retrieval Models: BM25 and Neural Reranking

-   Baseline Retrieval using BM25
    
-   Dense Retrieval using Bi-Encoder (neural reranker)
    

###  Evaluation Metrics Implementation

-   Precision and Recall
    
-   MAP (Mean Average Precision)
    
-   nDCG (Normalized Discounted Cumulative Gain)
    

###  Evaluation Results

 -   BM25: Precision, Recall, MAP, nDCG

 -   Bi-Encoder: Precision, Recall, MAP, nDCG
 
 
 ## Datasets
 The folder contains 2 datasets:
 
   **`advice_posts_def.csv`**:  Contains information about each post, including:
    
-   `query_id`: unique identifier for the post
        
-   `query_text`: the title of the post
        
-   `query_description`: detailed description of the post 


   **`advice_comments_def.csv`**:  Contains user-submitted comments associated with the posts, including:
    
-   `comment_id`: unique identifier for the comment
        
 -   `text`: the full comment text
        
-   `upvotes`, `karma_post`, `karma_comments`: voting and karma metadata
        
-   `timestamp`, `replies`: additional metadata


## Report
The report explains:
- Objective of the search engine.
- Strategies adopted for data collection.
- Models employed to develop the search engine and other modeling choices.
- Evaluation framework, metrics, and discussion.
