Task 2: Data Analysis with Complex Queries
In this task, we performed advanced data analysis using complex SQL queries involving multiple tables, subqueries, Common Table Expressions (CTEs), and window functions. The objective was to extract meaningful insights from movie data by identifying the top-rated movies per genre along with their respective directors.

The database consists of four tables: directors, movies, movie_directors, and ratings. The directors table stores information about each director, including a unique director_id and their name. The movies table includes details about movies such as movie_id, title, and genre. The movie_directors table is a mapping table that links each movie to its corresponding director, enabling a many-to-one relationship. The ratings table stores individual user ratings for each movie, identified by rating_id, associated movie_id, and a numeric rating on a scale from 1 to 10.

To derive insights, we constructed a SQL query using two Common Table Expressions (CTEs). The first CTE, named avg_ratings, computes the average rating for each movie, grouped by genre, title, and director. This is done by joining the movies, ratings, movie_directors, and directors tables and applying the AVG() function to calculate the average score. The result is rounded to two decimal places for better readability.

The second CTE, ranked_movies, uses the RANK() window function to rank the movies within each genre based on their average ratings in descending order. The PARTITION BY genre clause ensures that ranking is done within each genre separately.

Finally, the outer query selects only the top 2 movies per genre (i.e., where genre_rank <= 2) and outputs the genre, title, director name, and average rating. This result highlights the highest-performing movies in each genre and provides valuable insights for stakeholders like streaming platforms, production studios, or viewers interested in quality content.

This task effectively demonstrates the use of window functions, multi-table joins, and hierarchical query structuring via CTEs. It replicates real-world scenarios where data from multiple sources needs to be merged, aggregated, ranked, and filtered for analytical reporting. The final output serves as a compact and informative dashboard showing top-rated films by genre and their creators.


COMPANY: CODTECH IT SOLUTIONS

NAME: GNANA PREETHIKA A B

DOMAIN: SQL

DURATION: 4 WEEKS

MENTOR: NEELA SANTHOSH KUMAR
OUTPUT:
![Image](https://github.com/user-attachments/assets/554712f7-52d7-4d19-9d37-dee5ef2f4688)
