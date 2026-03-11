# Anime Recommendation System

## 1. Overview

Built a scalable recommender system on a highly sparse dataset (6.3M ratings) using:

Matrix Factorization (SVD)
TF-IDF + Cosine Similarity
Top-K ranking evaluation
Bias & novelty analysis

Designed under real memory constraints (sparse matrix optimization + stratified sampling).

The dataset was downloaded from Kaggle (https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database).
anime.csv - contains metadata of the anime such as the details of anime ID, name, genre, type and average rating
rating.csv - contains the user ratings for various anime, such as user ID, anime ID, and the ratings.


## 2. Scale

6.3M cleaned ratings
34K users
4.9K items
Extremely sparse user-item matrix
1% stratified sampling for efficient modeling


## 3. Models & Results (@Top-5, relevant ≥7)
SVD (Collaborative Filtering)

Precision: 0.72
Recall: 0.96
MAP: 0.95
NDCG: 0.98
Hit Rate: 1.0
Strong ranking accuracy
Popularity bias (low novelty)

Content-Based Filtering

Precision: 0.65
Recall: 0.99
MAP: 0.98
NDCG: 0.97
Hit Rate: 1.0
Genre-driven personalization
Lower catalog coverage


## 4. Key Insights

70% overlap in Top-10 recommendations
Weak ranking correlation → models capture different signals
Both models biased toward popular content
Hybrid approach would improve novelty & coverage


## 5. Tech Stack

Python • Pandas • NumPy • Scikit-learn • Surprise • SciPy



## 6. What This Demonstrates

Recommender system design
Matrix factorization
TF-IDF feature engineering
Sparse data handling
Hyperparameter tuning
Ranking metric evaluation
Bias analysis in recommendation systems
