# Movies-ETL
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. This porject created an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. The code from this module wsa refactored to create one function that takes in the three files; Wikipedia data, Kaggle metadata, and the MovieLens rating data, and performs the Extract, Transform, and Load process by adding the data to a PostgreSQL database.

## Deliverable One: Write an ETL Function to Read Three Data Files
This is a function test to ensure the ETL functions appropriatly (described as ETL_function_test.ipnyb).  Below are images of the dataframes from wiki_movies, kaggle_metadata, and ratings.
![Fig 1 - wiki_movies]()
![Fig 2 - kaggle_metadata]()
![Fig 3 - ratings]()

## Deliverable Two: Extract and Transform the Wikipedia Data
Using Python, Pandas, the ETL process, and code refactoring, the Wikipedia data was extracted and transformed, so it could be merged with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, a try-except block was also used to catch errors.
![Fig 4 - step 20]()
![Fig 5 - step 21]()
This is from file ETL_clean_wiki_movies.ipynb

## Deliverable Three: Extract and Transform the Kaggle Data
Using Python, Pandas, the ETL process, and code refactoring, the Kaggle metadata and MovieLens rating data was extracted and transformed.  We then converted the transformed data into separate DataFrames. The Kaggle metadata DataFrame was merged with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, we merged the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.
![Fig 6 - step 13 - same wiki_movies]()
![Fig 7 - step 14 movies_with_ratings_df]()
![Fig 8 - step 15 movies_df]()
This is from ETL_clean_kaggle_data.ipnyb

## Deliverable Four: Create the Movie Database
Using Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database as shown below.
Challenging item was installing the code to remove the ratings table in sql from python.  If this was not done each time the code was ran it kept adding to the 'ratings' sql table.  And with over 26+ million ratings the table could become quite large.
![Fig 9 - drop table]()
!Fig 10 - movies query]()
![Fig 11 - ratings query]()






