# Movie Recommendation Program

This is a simple movie recommendation program that utilizes a movie rating dataset to provide movie recommendations based on user preferences. The program uses Python and pandas library for data processing and analysis.

## Dataset
The program uses two datasets:
- `ratings.dat`: Contains information about movie ratings given by users. The dataset has columns like `userId`, `movieId`, `rating`, and `timestamp`.
- `movies.dat`: Contains information about movies, including their titles and genres. The dataset has columns like `movieId`, `title`, and `genres`.

Both datasets are downloaded from the following URLs:
- `ratings.dat`: [https://raw.githubusercontent.com/Arnavsmayan/Movie-Recommender/main/ratings.dat](https://raw.githubusercontent.com/Arnavsmayan/Movie-Recommender/main/ratings.dat)
- `movies.dat`: [https://raw.githubusercontent.com/Arnavsmayan/Movie-Recommender/main/movies.dat](https://raw.githubusercontent.com/Arnavsmayan/Movie-Recommender/main/movies.dat)

## Program Flow
1. The program starts by importing the necessary libraries: `pandas` and `numpy`.
2. The program reads the `ratings.dat` file using `pd.read_csv()` function and assigns column names: `userId`, `movieId`, `rating`, and `timestamp`.
3. It reads the `movies.dat` file using `pd.read_csv()` function and assigns column names: `movieId`, `title`, and `genres`.
4. The program merges the `rating` and `movie` dataframes using the `pd.merge()` function based on the common `movieId` column.
5. Unnecessary columns (`timestamp` and `movieId`) are dropped from the merged dataframe using the `drop()` function.
6. The program calculates the average rating and the number of reviews for each movie using the `groupby()` and `mean()` functions.
7. The program displays the first few rows of the resulting dataframe, showing the average rating and the number of reviews for each movie.

## Outputs
The program displays two outputs:
1. The first output is a dataframe that shows the average rating and the number of reviews for each movie. It includes columns: `title`, `Avg. Rating`, and `No. of Reviews`.
2. The second output is a dataframe that shows the average rating and the number of reviews for a subset of movies. It includes columns for each movie title and `userId`.

Note: The second output dataframe only shows a few movie titles and `userId` columns for brevity. The actual dataframe includes columns for all movies and `userId`.

Please refer to the code cells in the notebook for the actual implementation and execution of the program.
