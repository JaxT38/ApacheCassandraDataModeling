# Apache Cassandra Data Modeling

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

# Queries for Database Schema Design

Since the queries are known ahead of time and the amount of data is potentially in terabytes, denormalized tables are created in Cassandra. This will help generate queries faster and use fewer resources. There are 3 queries to begin with:

Query 1. I used 'sessionid' as the partition key and 'itemInSession' as my clustering key. Each partition is uniquely identified by 'sessionid' 
while 'itemInSession' was used to uniquely identify the rows within a partition to sort the data by the value of int.

Query 2. I used 'userId' and 'sessionid' as the composite partition key and 'itemInSession' as my clustering key. Each partition is uniquely identified by 'user id' and 'sessionid' while 'itemInSession' was used to uniquely identify the rows within a partition to sort the data by the value of int.

Query 3. I used 'song' as the partition key and 'userid' as my clustering key. Each partition is uniquely identified by 'song' while 'userid' was used to uniquely identify the rows within a partition to sort the data by the value of int.

