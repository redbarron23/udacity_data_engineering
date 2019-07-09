# Background

Sparkify provides a music streaming service to users. To enhance user experience and capture user preferences the following design is as follows:

- Fact Tables
consist of metric or facts these are usually static in nature and are not meant to be updated
Data types are usually comproised of ints

- Dimension Tables
is a structure that categorises facts and measures in order to enable users to answer business questions. Dimensions are people, products, place and time

- Star Schema
is a topology that consists of one more more fact tables referencing any number of dimension tables.

# Purpose

Create an organised data model that will simplfly queries and denormalise data.
The following steps will be used to accomplish this requirement.

1. Create a data model using a star schema that includes fact and dimension tables.

2. Write an ETL pipeline that loads and transfers data from two local directories into these aforemetioned tables.

3. Provide example queries for analytics.

# Schema Design

## Fact Table

- songplays - records in log data associated with song plays.

## Dimension Tables

- users - users in the app
- songs - songs in music database
- artists - artists in music database
- time - timestamps of records in songplays broken down into specific units

![Alt text](img/udacity_project1.png?raw=true "Title")

# ETL PipeLine

## Log Data

The log data files contains all the information about specific user sessions. This information contains info about what songs were listened to and at what time. User data is captured including name, location, subscription,status and web browser info.

## Song Data

The song data files contain information about specific songs. such as artist, duration, and the artists location.

## Setup

Data is stored on local disk and is in json format and is retrieved by walking a directory and putting into panda data frames

```python3 create_tables.py```

```python3 etl.py```

are executed to create the tables and load the data

## Misc items include Jupyter notedbooks

etl.ipynb - Useful for developing and testing ETL Pipelines

test.pynb - Testing and querying DB for info

# Example Queries and results

[Optional] Provide example queries and results for song play analysis.