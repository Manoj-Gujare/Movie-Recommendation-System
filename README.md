# Movie Recommendation System

## Description
This project implements a movie recommendation system using content-based filtering. The system suggests movies similar to the input movie based on various attributes such as cast, crew, genres, and keywords. The recommendation system is built using Python and utilizes natural language processing (NLP) techniques to analyze and process movie attributes.

## Tools & Libraries
- Python (Version 3.x)
- Pandas
- NumPy
- Natural Language Toolkit (NLTK)
- Scikit-learn
- Pickle
- Streamlit

## Dataset
The dataset used for building the recommendation system consists of two CSV files: `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`. These files contain information about movies, including details about cast, crew, genres, keywords, and overview.

## Data Preprocessing
- The datasets are loaded using Pandas and merged based on the movie title.
- The cast, crew, genres, keywords, and overview columns are preprocessed by cleaning, tokenizing, and converting to lowercase.
- Text data is stemmed to reduce words to their root form for better analysis.
- Features such as cast, crew, genres, and keywords are combined to create a consolidated attribute called `all_tags`.

## Feature Engineering
- The `all_tags` attribute is vectorized using CountVectorizer to convert text data into numerical features.
- Cosine similarity is calculated between the vectorized features to measure the similarity between movies.

## Movie Recommendation
- The movie recommendation system is deployed using Streamlit, providing an interactive interface for users to input a movie title and receive recommendations.
- Based on the input movie, the system calculates the cosine similarity with other movies and recommends the most similar ones.
- The top recommended movies along with their posters are displayed to the user.

## Usage
To use the movie recommendation system:
1. Run the Streamlit app by executing the Python script containing the Streamlit code.
2. Select a movie title from the dropdown menu.
3. Click the "Recommend" button to view recommended movies similar to the selected one.
4. Recommended movies along with their posters will be displayed on the interface.

## Model Persistence
The processed dataset and calculated similarity matrix are saved using the Pickle library for future use.
