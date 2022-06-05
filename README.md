# Module 8 - Movies ETL Challenge

## Overview
The purpose of this challenge is to become familiar with the "Extract, Transform, and Load" process throughout the data pipline.
In this process, we must first extract movie data from JSON or CSV files saved in certain directories. Then, we filter, merge, and analyze the data provided by using functions, list comprehension, and regex expressions. Finally, we establish a connection to our local SQL database in order to upload our final copies of merged data into the 'movies' table and 'ratings' table.

When we successfully extract data from the internet by using API calls or dowloading CSV files, we must then put the data into a Data Frame object in order to successfully transform the data. Data transformation can entail deleting redundant columns, replacing empty cell values, extracting certain values, and etcetera.

Finally, we must carefully merge the dataframes from several files into 1 dataframe that can be uploaded onto the database as the 'movies' table. At the same time, we also learn good practices in uploading large datasets such as the ratings.csv file into the Postgres SQL database.

## Special notes
- The ratings.csv file was left off the final git upload since the dataset was too large.
- On module challenge 8 - Deliverable 4 where we have to create a new ETL_create_database.ipynb file, there is step 2: Remove the statement return wiki_movies_df, movies_with_ratings_df, movies_df. Since the return statement had to be deleted, I had to perform the following steps in order for the remainder of the code in the ETL_create_database.ipynb file to show the dataframes:

1.) Re-download my solved ETL_clean_kaggle_data.ipynb file as a .py file and saved it to the directory of my project.  
2.) Import that file into the ETL_create_database.ipynb as:  
```import ETL_clean_kaggle_data as etl```
3.) Set up step 12 of the code as:  

```
# 12. Set the DataFrames from the return statement equal to the file names in Step 11. 
wiki_movies_df = etl.wiki_movies_df
movies_with_ratings_df = etl.movies_with_ratings_df
movies_df = etl.movies_df
```

This was the only way I could call variables from the ETL_clean_kaggle_data.ipynb file to the ETL_create_database.ipynb if we're removing the "return" statement.
