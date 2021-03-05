# Apache Cassandra Data Modeling

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

# Database Schema Design

Since the queries are known ahead of time and the amount of data is potentially in terabytes, denormalized tables are created in Cassandra. This will help generate queries faster and use fewer resources. There are 3 queries to begin with:

1. Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

