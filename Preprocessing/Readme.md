# Preprocessing

This notebook is used for the preprocessing of the data. It has to be used before running the Dashboard and the Classifiers.

This code performs various data preprocessing and analysis tasks on datasets related to IMDb movie reviews and information about the top 250 movies. It employs the Python libraries pandas, nltk, and transformers for data manipulation, natural language processing, and data analysis.

The code's primary steps are as follows:

1. Load and Prepare Datasets: The code loads two CSV datasets: one containing movie reviews (df_reviews_top_250.csv) and another containing information about the top 250 movies (df_top_250_movies.csv). It drops unnecessary columns and handles missing values.
2. Data Quality Checks: The code checks the data quality by examining any non-string values in specific columns of the datasets (IMDB_Reviews_Top_250_preprocessed.csv).
3. Preprocessing and Stopword Removal: Stopwords from the NLTK library are downloaded. A function is defined to remove stopwords from review titles and texts. Stopword removal is applied to the review data, resulting in preprocessed versions with and without stopwords.
4. Data Aggregation: The code aggregates the review data to find the number of reviews and the average ratings for each movie title.
5. Merge Datasets: The aggregated review data is merged with the information about the top 250 movies dataset to create a comprehensive dataset (df_info_top_250_full.csv) containing each movie's reviews, ratings, and other details.

The technologies that were used are:

1. pandas: This library is used for data manipulation, cleaning, and aggregation.
2. nltk (Natural Language Toolkit): It's used for text preprocessing, including downloading stopwords and tokenizing words.

The code aims to preprocess, clean, and aggregate data from IMDb movie reviews and top movie information into a unified dataset for further analysis.

The reviews dataset without the stopwords is here (IMDB_Reviews_Top_250_preprocessed_without_stopwords.csv):

https://drive.google.com/drive/folders/1G2uLriXt7z-_RRn8qn1cOaWYQVZRVR5-

