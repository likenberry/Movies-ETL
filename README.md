# Movies ETL

## Overview of Analysis

The purpose of this analysis was to extract data for an analysis, transform it into a usable form and load it into a database. This analysis was performed on data gathered from Wikipedia and Kaggle in a JSON file and a csv file. These files were transformed using Pandas in Jupyter Notebook. All of the data sources needed to be combined into a single homologous data set. The data sources had different data formats and various columns had similar data but different names that had to be combined. Other data had to be filtered or removed because it was corrupt or unneccessary for this analysis. Various functions including lambda and regular functions (regx) were used to transform various aspects of these data files. Once all of the columns were of the same data type and similar name, it was time to decide which column would be kept in the final data set. This is a table of where the data from each column came from for the final combine data set.
![Table of Column Data Source](https://github.com/likenberry/Movies-ETL/blob/main/Resources/Final_Data_Columns.png)
Once the final data set was merged and cleaned, it was loaded into Postgresql (SQL) using SQLAlchemy and the Pandas function .to_sql. The two tables that were loaded into SQL was a movies table and a ratings table. Finally, in order to check that all of the rows were correctly loaded into SQL, a count of all the data in each table was performed. Below are the images of the counts of the tables confirming that all the data was successfully loaded into SQL.
![Count of Movies Table](https://github.com/likenberry/Movies-ETL/blob/main/Resources/movies_query.png)
![Count of Ratings Table](https://github.com/likenberry/Movies-ETL/blob/main/Resources/ratings_query.png)

## Resources

- Data Source: movies_metadata.csv, ratings.csv, wikipedia-movies.json
- Software: pgAdmin 4 Version 6.1, Visual Studio Code 1.62.1, Jupyter Notebook
