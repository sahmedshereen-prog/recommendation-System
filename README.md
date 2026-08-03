# Movie Recommendation System

A recommendation system for a movie platform using two complementary approaches.

## Overview
- **Goal**: Build a recommendation system for a movie or product platform.
- **Data**: [MovieLens (latest-small)](https://www.kaggle.com/datasets/grouplens/movielens-latest-small)
  - `movies.csv` (movieId, title, genres)
  - `ratings.csv` (userId, movieId, rating, timestamp)

## Approach
Two recommendation approaches are implemented and compared:

1. **Collaborative Filtering (item-based)**
   Recommends movies based on how other users with similar taste rated them, using cosine similarity between movies on the user-rating matrix. Evaluated with **RMSE** on a held-out test set.

2. **Content-Based Filtering**
   Recommends movies similar in genre to a movie the user liked, using TF-IDF on genres + cosine similarity. Evaluated qualitatively by inspecting the top similar movies for a sample title.

## How to run
No extra installation needed if running on Google Colab (pandas, numpy, scikit-learn are pre-installed). Locally:
```bash
pip install pandas numpy scikit-learn
```
1. Place `movies.csv` and `ratings.csv` in this folder.
2. Run:
```bash
python recommendation_system.py
```

## Outputs
- Predicted RMSE for the collaborative filtering model, printed to console
- Top-10 collaborative-filtering recommendations for a sample user
- Top-10 content-based recommendations similar to a sample movie

## Author
Uneeq Interns Task Submission
