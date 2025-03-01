Spotify Data Engineering Pipeline - README
Overview
This project implements a data engineering pipeline on Amazon Web Services (AWS) to process Spotify data. The pipeline involves ingesting CSV files containing information about artists, tracks, and albums into an S3 bucket, performing ETL (Extract, Transform, Load) operations using AWS Glue, storing the transformed data in Parquet format, and finally querying and visualizing the data using Amazon Athena and Power BI.

Components
1. Data Source
CSV Files: Manually upload CSV files containing details of artists, tracks, and albums to an S3 bucket.
2. AWS Services
Amazon S3 (Simple Storage Service)
Serves as the storage repository for raw CSV files.
AWS Glue
ETL Process: Extracts, transforms, and loads data.
ETL Script: Performs inner joins on artist, track, and album datasets.
Output Format: Saves processed data in Parquet format for efficient querying.
IAM Role: Assigns appropriate permissions to allow Glue to access and write data to S3.
AWS Glue Crawler
Infers the schema of Parquet files and creates metadata tables in the AWS Glue Data Catalog.
Amazon Athena
Queries Parquet files stored in S3 to analyze Spotify data using SQL.
3. Data Visualization
Power BI
Connects to Amazon Athena to create dashboards and visualize processed Spotify data.
Setup Instructions
Step 1: Upload CSV Files to S3
Manually upload CSV files containing artist, track, and album data to the designated S3 bucket.
Step 2: Configure AWS Glue ETL Job
Create an AWS Glue ETL job.
Develop an ETL script to perform inner joins on the artist, track, and album datasets.
Store the transformed data as Parquet files in a separate S3 bucket.
Assign appropriate IAM roles to allow Glue to access and write data.
Step 3: Set Up AWS Glue Crawler
Create an AWS Glue Crawler to infer the schema of Parquet files.
Run the crawler to generate metadata tables in the AWS Glue Data Catalog.
Step 4: Query Data with Amazon Athena
Connect Amazon Athena to the S3 bucket storing Parquet files.
Execute SQL queries to analyze and extract insights from the Spotify data.
Step 5: Visualize Data with Power BI
Connect Power BI to Amazon Athena as a data source.
Create dashboards and visualizations to represent insights derived from the Spotify data.
Notes
Ensure IAM roles and permissions are correctly configured for S3, Glue, and Athena.
Monitor AWS costs, particularly data storage and query execution expenses.
Regularly update the pipeline to accommodate changes in data structure or evolving requirements.