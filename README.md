# Movie Recommendation System

This repository contains a movie recommendation system implemented using different techniques such as content-based filtering, collaborative filtering, and matrix factorization.

## Table of Contents

- [Description](#description)
- [Technologies](#technologies)
- [Files](#files)
- [Usage](#usage)
- [Examples](#examples)

## Description

This project aims to recommend similar movies to users based on a variety of approaches:

1. **Content-Based Filtering**: Using movie metadata (genres, tags, etc.), movies with similar characteristics are recommended.
2. **Collaborative Filtering**: This method uses user ratings to recommend movies that users with similar preferences have rated highly.
3. **Hybrid Model**: A combination of content-based and collaborative filtering to improve the accuracy of recommendations.
4. **Popularity-Based Recommendations**: Suggesting movies that have received the most ratings or highest user engagement.
5. **Matrix Factorization**: Using techniques like Singular Value Decomposition (SVD) to decompose the user-movie matrix and predict ratings for unseen movies.

## Technologies

This project uses the following libraries:
- `pandas` for data manipulation
- `numpy` for numerical operations
- `scikit-learn` for implementing TF-IDF, SVD, and cosine similarity
- `matplotlib` (optional, for visualization)
- `seaborn` (optional, for visualization)

## Files

- **movies.csv**: Contains metadata about movies, including `movieId`, `title`, and `genres`.
- **ratings.csv**: Contains user ratings for movies, including `userId`, `movieId`, and `rating`.
- **tags.csv**: Contains user-generated tags for movies, including `userId`, `movieId`, and `tag`.
- **code.py**: The Python script containing all functions for generating movie recommendations.

## Usage

To use this recommendation system, follow the steps below:

### Step 1: Install the required libraries

Make sure to install all necessary libraries. You can install them using `pip`:

```bash
pip install pandas numpy scikit-learn

Step 2: Load the data
Ensure that the movies.csv, ratings.csv, and tags.csv files are placed in the same directory as the script. The data is loaded into pandas DataFrames as follows:

movies_metadata = pd.read_csv('movies.csv', nrows=100000)
ratings = pd.read_csv('ratings.csv', nrows=100000)
tags = pd.read_csv('tags.csv', nrows=100000)

Step 3: Generate recommendations
Content-Based Recommendations: Call the recommend_similar_movies(title) function to recommend movies based on a given movie title.

Popularity-Based Recommendations: Call the popularity_recommender(movies_metadata, ratings, top_n=10) function to get the top 10 popular movies based on user ratings.

Matrix Factorization-Based Recommendations: Call the matrix_factorization_recommender(user_id, user_movie_matrix, top_n=10) function to recommend movies to a specific user using matrix factorization.


