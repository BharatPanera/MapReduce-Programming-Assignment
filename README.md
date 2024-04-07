# MapReduce Programming Assignment

This assignment focuses on utilizing big data tools such as Hadoop Framework, Apache HBase, and Apache Sqoop to analyze the NYC TLC yellow taxi dataset for the year 2017. The dataset includes detailed trip records and related information.

## Dataset Description

The NYC TLC yellow taxi dataset for 2017 comprises multiple CSV files, each representing trip data for a specific month. The dataset can be accessed from the following links:

```
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-01.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-02.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-03.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-04.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-05.csv
https://nyc-tlc-upgrad.s3.amazonaws.com/yellow_tripdata_2017-06.csv
```

## Tasks

### Data Ingestion Tasks:

#### Task 1. Create an RDS instance in your AWS account and upload the data to the RDS instance.

- **Description**: Create an AWS RDS instance and upload trip data from two CSV files (yellow_tripdata_2017-01.csv & yellow_tripdata_2017-02.csv).
- **Steps**:
  1. Set up an appropriate schema based on the [data dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf)
  2. Create an RDS instance in your AWS account using the appropriate settings.
  3. Upload the selected CSV files to the RDS instance.

#### Task 2. Use Sqoop command to ingest the data from RDS into the HBase Table.

- **Description**: Ingest data from the RDS instance into the HBase Table using Apache Sqoop.

#### Task 3. Bulk import data from the next two files in the dataset on your EMR cluster to your HBase Table using the relevant codes.

- **Description**: Import data from the subsequent two CSV files (yellow_tripdata_2017-03.csv & yellow_tripdata_2017-04.csv) on your EMR cluster.

### MapReduce Tasks:

#### Task 4. Write MapReduce codes to perform the following tasks using the files downloaded on your EMR Instance:

1. **Which vendors have the most trips, and what is the total revenue generated by that vendor?**
2. **Which pickup location generates the most revenue?**
3. **What are the different payment types used by customers and their count? The final results should be in a sorted format.**
4. **What is the average trip time for different pickup locations?**
5. **Calculate the average tips to revenue ratio of the drivers for different pickup locations in sorted format.**
6. **How does revenue vary over time? Calculate the average trip revenue per month - analyzing it by hour of the day (day vs night) and the day of the week (weekday vs weekend).**

- **Note**: It's recommended to use MRJob for completing the MapReduce tasks above.

### Optional Task:

#### Task 5. Use Sqoop export command to export the results of each MapReduce task above to your RDS instance. Use the RDS connection string to visualize the dataset using a dashboarding tool (Google Data Studio, Tableau, or PowerBI).

- **Description**: Export the results of each MapReduce task to your RDS instance and visualize the dataset using a dashboarding tool.

## Evaluation Rubric

Each task will be evaluated based on completeness, accuracy, efficiency, and adherence to best practices in big data processing.