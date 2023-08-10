# IMDB Reviews' Scraper

This a scraper for all the reviews of the top 250 movies on IMDB based on popularity. It provides all the reviews without any preprocessing. 

This code performs web scraping on the IMDb website to extract information about the top 250 movies and their reviews. It utilizes the Python libraries pandas and selenium for data manipulation and web automation, respectively, and the webdriver-manager to manage the web driver required for browser automation.

The main steps of the code are as follows:

1. It initializes a Chrome web driver using the webdriver-manager library.
2. It scrapes information from the IMDb page containing the top 250 movies, including movie titles, indexes, release years, links, reviews links, and genres. This data is stored in lists and then used to create a pandas DataFrame.
3. The script then navigates to each movie's reviews page and iteratively scrolls to load more reviews until all reviews for that movie are retrieved. The reviews' titles, texts, and ratings are extracted and stored in lists.
4. The extracted review data is used to create another pandas DataFrame.
5. The final movie details and review data are saved in CSV files named '250_top_movies.csv' and '250_top_movies_reviews_raw.csv', respectively.
The code leverages the Selenium library to automate web interaction, including scrolling and clicking on "Load More" buttons to retrieve reviews. It also utilizes the pandas library to store and manipulate the extracted data in tabular form efficiently. Additionally, the webdriver-manager package helps manage the browser driver necessary for Selenium automation.

The raw dataset is available in the following link:

https://drive.google.com/drive/folders/1G2uLriXt7z-_RRn8qn1cOaWYQVZRVR5-?usp=sharing

The scraper was based on Selenium. More about Selenium can be found in the following link:

https://www.selenium.dev/

The last run of this scraper was on 14/07/2023. 
