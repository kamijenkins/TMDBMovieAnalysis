Code Louisville - Python for Data - Final Project
Kami Jenkins

##### Required Dependancies
- Python 3.7.1
- Anaconda
- JupyterNotebook
- pandas
- sqlite3
- numpy
- matplotlib

- bokeh (not really for the project, but what I have been working on since fulfilling the requirements)

### PROJECT QUESTION
Are female actresses evenly represented amongst the Actors/Actresses that are in the most movies in this database?

### SOURCE
- This csv file is from kaggle, but the dataset if from TMDb which contains 4803 movies and 20 rows.  The file is included in the project folder on github for easy access to run, but was originally gathered from https://www.kaggle.com/tmdb/tmdb-movie-metadata
The csv file is included in my github to make it easier to run.

### ANALYSIS
##### Loading the csv and sorting data
- In order to turn my csv file into useable information, I first decided on my project scope and filtered the initial 20 columns down to 14 that contained applicable information.

##### Prepairing the data
- I dropped all of the null values and duplicate rows to help with my analysis.
- Format Column names

##### SQL
- Created SQL database named tmdb and a table in database also named tmdb.  I checked to see if the table exists to avoid an error when you try to create a table that already exists.
- Used SQL to create a pandas DataFrame that contained 2 columns (Director and Frequency) from the original database.  This way I was able to compute the number of movies in the dataset that each director has made, and sort them descending to find the directors with the most movies
- Used SQL to find the top 10 grossing movies
- Found unique actors in database (3707)
- Found unique directors in database (1707)
- Calculated Actors that appear in the most movies in that database.  This task wasn't as straightforward as doing the similar thing with directors.  In the original dataset there are 3 different columns that contain actor names (unlike directors that only have 1) so I had to use SQL Unions to combine the 3 actor columns, then run computations to find the ones that appear with the greatest frequency.

### GRAPHS
I based my matplotlib and bokeh graphs on the basic documentation examples for both respective libraries.  Here I graph all of the data that I analyzed in the last section

### CONCLUSION
By looking at the data returned, it appears that actresses are not represented in any way in the top 10 most frequent actors listed in the database.  
