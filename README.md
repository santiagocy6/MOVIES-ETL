# MOVIES-ETL

## Overview
I will create a pipeline that Extract, Transform and Load teh data into existing tables. I will create one function that takes in the three files: movies_metadata, ratings, and wikipedia_movies. After that, I will perform the ETL process by adding the data to a PostgreSQL database. 

## Deliverable 1: Write an ETL Function to Read Three Data Files
During the ETL_function_test, I created a code that read all the data that I have in the CVS, TXT and JSON files, then I define the Dataframes to have th access and check them, with this I got the following results: 
wiki_movies = 5 rows * 193 columns 
Kaggle_metadata = 24 * 24 columns 
ratings = rows * 4 columns

## Deliverable 2: Extract and Transform the Wikipedia Data
On this deliverable ETL_clean_wiki_movies, as the name says we did a code to clean movie function using a Key that countains the info in alt_titles and I change the name in movie getting the following outputs:
wiki_movies = 5 rows * 23 columns 
wiki_movies_df.columns = ['url',
 'year',
 'imdb_link',
 'title',
 'Based on',
 'Starring',
 'Cinematography',
 'Release date',
 'Country',
 'Language',
 'Budget',
 'Director',
 'Distributor',
 'Editor(s)',
 'Composer(s)',
 'Producer(s)',
 'Production company(s)',
 'Writer(s)',
 'imdb_id',
 'box_office',
 'budget',
 'release_date',
 'running_time']


## Deliverable 3: Extract and Transform the Kaggle data
On this step ETL_clean_kaggle_data gets new tasks for cleaning Kaggle data and includes:
- Changing datatypes, using methods pd.to_numeric, astype() and python comparison operators for Boolean types.
- Filling missing values and filtering unwanted columns.
- Merging data frames using pd_merge method.

## Deliverable 4: Create the Movie Database
FInally I send all the cleaned and marged datasets to PostgreSQL and I created and DataBase movie_data that counts all the rows in ratings:(26024289) and  movies:(6052) as we can see in the queries that I added. 

