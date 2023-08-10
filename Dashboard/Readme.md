# IMDB Top 250 Movies Dashboard

This Dashboard overviews the Top 250 Movies on IMDB based on their popularity. It is based on Dash Plotly and presents insights and visualizations based on the dataset containing information about the top 250 movies on IMDb.

The code performs the following steps:

1. It imports the necessary libraries, including Dash, Plotly, and pandas.
2. Loads two datasets, one containing movie information and another containing movie reviews (available here: https://drive.google.com/drive/folders/1G2uLriXt7z-_RRn8qn1cOaWYQVZRVR5-).
3. Splits the "Genre" column of the movie dataset into three separate columns: "Genre 1," "Genre 2," and "Genre 3."
4. Converts the movie ratings into binary values based on a specified threshold (7).
5. Defines functions to count the number of words in review titles and texts.
6. Creates a bar chart to show the number of movies released per year.
7. Creates various visualizations, including pie charts for movie genres, violin plots for rating distribution, and animated bar charts for movies sorted by review counts.
8. It provides an interactive dropdown to select a movie and displays its details, such as position, rating, year, reviews, and links to the IMDb page.
9. Allows the user to select a movie for review analysis and displays average, maximum, minimum, and standard deviation values for rating, review title word count, and review text word count.
10. Displays violin plots for review rating, review title word count, and review text word count for the selected movie.

The code further sets up the Dash app's layout with two tabs: "Movies Overview" and "Reviews Overview." The "Movies Overview" tab provides visualizations and leaderboards related to movies, while the "Reviews Overview" tab focuses on review-related insights. The app includes interactive elements, allowing users to select specific movies and view corresponding details and visualizations.

Technologies used:

1. Dash: A Python web application framework for building interactive web applications with visualizations.
2. Plotly: A graphing library that creates interactive, publication-quality visualizations.
3. pandas: A powerful data manipulation library for Python.
