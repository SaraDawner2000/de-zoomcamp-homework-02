# de-zoomcamp-homework-02
Natalie Demyanenko, week 2 homework

## Question 1
After backfilling the data workflows through Kestra, I located the "yellow_tripdata_2020-12.csv" file in the GCP storage bucket for this project. 

**Answer:** 128.3 MB
## Question 2
After the filename is rendered, the input values are interpolated into it.

**Answer:** "green_tripdata_2020-04.csv"
## Question 3
In BigQuery, I ran:
```sql
SELECT COUNT(*)
FROM ndzoomcamp_dataset.yellow_tripdata
WHERE EXTRACT(YEAR FROM tpep_dropoff_datetime) = 2020;
```
The result was 24,648,109, which is smaller than the given option of 24,648,499, maybe because there were duplicates or other problems in the csv files.

**Answer:** 24,648,499
## Question 4
In BigQuery, I ran:
```sql
SELECT COUNT(*)
FROM ndzoomcamp_dataset.green_tripdata
WHERE EXTRACT(YEAR FROM lpep_pickup_datetime) = 2020;
```
The result was 1,734,039, which is smaller than the given option of 1,734,051, maybe because there were duplicates or other problems in the csv files.

**Answer:** 1,734,051
## Question 5
In BigQuery, I ran:
```sql
SELECT COUNT(*)
FROM ndzoomcamp_dataset.yellow_tripdata
WHERE EXTRACT(YEAR FROM tpep_dropoff_datetime) = 2020;
  AND EXTRACT(MONTH FROM tpep_dropoff_datetime) = 3;
```
The result was 1,925,076, which is smaller than the given option of 1,925,152, maybe because there were duplicates or other problems in the csv files.

**Answer:** 1,925,152
## Question 6
From [Kestra documentation](https://kestra.io/plugins/core/triggers/io.kestra.plugin.core.trigger.schedule) on the timezone property of the Schedule trigger:

>The time zone identifier (i.e. the second column in [the Wikipedia table](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)) to use for evaluating the cron expression. Default value is the server default zone ID.

**Answer:** America/New_York 
