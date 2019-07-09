# Purpose
1. Create a data model using a star schema that includes fact and dimension tables
2. Write an ETL pipeline that loads and transfers data from two local directories 
   into these aforemetioned tables
3. run queries for analytics

# Schema Design and ETL PipeLine
State and justify your database schema design and ETL pipeline.

- Fact Table

songplays - records in log data associated with song plays i.e. records with page NextSong
+-------------+------------+
|  songplays  |    type    |
+-------------+------------+
| songplay_id |  serial    |
| start_time  |  timestamp |
| user_id     |  int       |
| level       |  char(4)   |
| song_id     |  text      |
| artist_id   |  text      |
| session_id  |  int       |
| location    |  text      |
| user_agent  |  text      |
+-------------+------------+

- Dimension Tables

users - users in the app
+------------+----------+
|   users    |   type   |
+------------+----------+
| user_id    |  int     |
| first_name |  text    |
| last_name  |  text    |
| gender     |  char(1) |
| level      |  char(4) |
+------------+----------+

songs - songs in music database
+-----------+-------+
|   songs   |  type |
+-----------+-------+
| song_id   |  text |
| title     |  text |
| artist_id |  text |
| year      |  int  |
| duration  |  text |
+-----------+-------+

artists - artists in music database
+-----------+----------+
|  artists  |   type   |
+-----------+----------+
| artist_id |  text    |
| name      |  text    |
| location  |  text    |
| latitude  |  numeric |
| longitude |  numeric |
+-----------+----------+

time - timestamps of records in songplays broken down into specific units
+------------+------------+
|   times    |    type    |
+------------+------------+
| start_time |  timestamp |
| hour       |  int       |
| day        |  int       |
| week       |  int       |
| month      |  int       |
| year       |  int       |
| weekday    |  int       |
+------------+------------+


# Example Queries and results
[Optional] Provide example queries and results for song play analysis.

