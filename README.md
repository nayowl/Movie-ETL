# Movie-ETL
## 1 Overview of The Project
Amazing Prime Video was a platform for streaming movies and TV shows.They want so sponsor a hackathon providing a clean data set of movie data. To provide the clean data sets the Amazing Prime video will follow the ETL process: Extract the Wikipedia and Kaggle data from their respective files,  transform the datasets by cleaning them up and joining them together, and load the cleaned dataset into a SQL database. In this analysis, the goal is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables.

The following tasks will be performed in this analysis:
1. Write an ETL Function to Read Three Data Files
2. Extract and Transform the Wikipedia Data
3. Extract and Transform the Kaggle data
4. Create the Movie Database

## 2 Resources
Software: Python 3.7.6 , Jupyter notebook, Pandas library, SQL, pgAdmin4

## 3 Results
1. Write an ETL Function to Read Three Data Files
   * The function will be named Read_data() 
   * It will read two csv data files and one json file : movies_metadata.csv,ratings.csv,wikipedia-movies.json
   * The data will be transformed into three pandas dataframe wiki_movies_df,kaggle_metadata,ratings
2. Extract and Transform the Wikipedia Data
   * The function will be named read_clean_data()
   * It will read two csv data files and one json file : movies_metadata.csv,ratings.csv,wikipedia-movies.json
   * In this function :
      *  it will call function clean_movie() that combines alternative languages columns to one columns alt_titles and change some column names
      *  extract imdb_id and drop duplicate if any
      *  write a list of comprehension to keep the columns that don't have null values from the wiki_movies_df
      *  Clean box office, budget, release date and running time column by using regular expression
5. Extract and Transform the Kaggle data
   * The function will be named Read_kaggle_wiki_rating_data()
   * It will read two csv data files and one json file : movies_metadata.csv,ratings.csv,wikipedia-movies.json
   * In this function :
      *  it will call function clean_movie() that combines alternative languages columns to one columns alt_titles and change some column names
      *  extract imdb_id and drop duplicate if any
      *  write a list of comprehension to keep the columns that don't have null values from the wiki_movies_df
      *  Clean box office, budget, release date and running time column in wiki_movies_df by using regular expression
      *  Clean the kaggle metadata by change the current datatype to the right datatype
      *  Merge wiki_movies_df and kaggle_data to movies_df dataframe , drop unnecessary column and fill missing data in the new dataframe
      *  Transform and merge ratings dataframe with movies_df and creating a new  movies_with_ratings_df dataframe 
7. Create the Movie Database
 * The function will be named Read_Transfer_Data()
   * It will read two csv data files and one json file : movies_metadata.csv,ratings.csv,wikipedia-movies.json
   * In this function :
      *  it will call function clean_movie() that combines alternative languages columns to one columns alt_titles and change some column names
      *  extract imdb_id and drop duplicate if any
      *  write a list of comprehension to keep the columns that don't have null values from the wiki_movies_df
      *  Clean box office, budget, release date and running time column in wiki_movies_df by using regular expression
      *  Clean the kaggle metadata by change the current datatype to the right datatype
      *  Merge wiki_movies_df and kaggle_data to movies_df dataframe , drop unnecessary column and fill missing data in the new dataframe
      *  Transform and merge ratings dataframe with movies_df and creating a new  movies_with_ratings_df dataframe 
      *  Create movie and ratings database in pgAdmin by importing it from movies_df and ratings  
