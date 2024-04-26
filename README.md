# Overview

The purpose of this project is to leverage the power of Python, in conjunction with Jupyter Notebook, to integrate movie reviews from The New York Times with comprehensive movie details from The Movie Database (TMDB). This integration provides a holistic view of movies, combining critical reviews with detailed metadata. By merging these datasets, users can gain insights into various aspects of movies, such as genres, languages, production countries, and critical reception.

# Functionality

1. Imports and Setup:
    - The project begins by importing necessary libraries such as requests, time, dotenv, os, pandas, and json.
    - Environment variables are set up using dotenv to securely access API keys required for accessing NYT and TMDB APIs.
2. Fetching NYT Reviews:
    - The code constructs a URL for accessing NYT movie reviews based on specified criteria such as section name, type of material, and search keywords.
    - It retrieves the reviews from the API, looping through multiple pages to gather all available data, and stores them in a list.
3. Fetching TMDB Movie Details:
    - TMDB queries are prepared, and an empty list is initialized to store the results.
    - The code iterates through the list of movie titles extracted from NYT reviews, makes requests to TMDB API to fetch detailed movie information, including genres, languages, and production countries.
    - If a movie is not found in the TMDB database, a message is printed.
4. Merging DataFrames:
    - The code merges the DataFrame containing NYT reviews with the DataFrame containing TMDB movie details based on movie titles.
    - Unnecessary columns like "byline.person" are dropped, duplicate rows are removed, and the index is reset.
5. Data Formatting and Exporting:
    - Certain columns containing lists, such as genres, spoken languages, and production countries, are formatted by removing list brackets and quotation marks.
    - The final DataFrame is exported to a CSV file without including the index, facilitating further analysis or sharing of the data.

# Summary

This project demonstrates the capability of Python and Jupyter Notebook in integrating and analyzing diverse datasets. The merged dataset provides a rich resource for understanding various aspects of movies, from critical reception to production details. Professionally, similar approaches can be employed in market research, recommendation systems, or content curation for movie platforms. Personally, movie enthusiasts can use such analyses for exploring their favorite movies, discovering new ones, or gaining insights into trends in the film industry.