# Movie-Recommendation-System

##Objective

To recommend movies similar to a selected movie for a specific user, ensuring that the suggestions are relevant and not already rated by the user.

##Dataset

Source: MovieLens 100K dataset
https://grouplens.org/datasets/movielens/

Size: 100,000 ratings by 943 users on 1,682 movies

Includes: Ratings (1–5), movie metadata, and user demographics

##Approach

1. Data Loading & Cleaning
- Parsed and merged u.data (ratings) with u.item (movie titles).
- Removed duplicates and handled missing values.
2. User-Movie Matrix
- Created a matrix with users as rows, movie titles as columns, and ratings as values.
- Filled missing ratings with 0 for sparse matrix representation.
3. Item-Based Collaborative Filtering
- Computed cosine similarity between movie vectors (columns of the matrix).
- Built a similarity matrix capturing how similarly movies are rated by all users.
4. Recommendation Logic
- For a given movie and user, Retrieved top-N similar movies, Filtered out movies already rated by the user.
- Returned the top recommended titles.
5. Personalization
- Ensured that recommendations are specific to each user by excluding their watched/rated movies.
