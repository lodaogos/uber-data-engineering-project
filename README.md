# Uber Data Engineering Project

![Uber Logo](./assets/uber%20logo.jpg)

## Introduction

This is my personal project in order to further amplify my understanding towards data engineering especially in using ETL pipeline thanks to 
Darshil Parmar Tutorial on Youtube. The tools that will be used on this project are Jupyter Notebook, GCP Storage, Python, Compute Instance, Mage AI, BigQuery, and Looker Studio.

## Dataset Used

We will use NYC TLC Trip Record dataset for this project. The dataset contains yellow and green taxi trip records which include fields that capture pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

The dataset used for this project can be found here: https://github.com/lodaogos/uber-data-engineering-project/blob/main/data/uber_data.csv

More information about the dataset can be found here:
1. TLC Website: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
2. TLC Data Dictionary: https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Data Modelling Using draw.io
In order to use our dataset efficiently, we can first create a data model by dividing the data into dimension table and fact table. In data warehousing, a dimension table is a database table that stores attributes describing the facts in a fact table. Fact table usually contains the FK of a dimension table. In addition to these foreign keys, the fact table also contains measures or facts, which are often numeric and used for analysis. You can read more about it here: https://www.simplilearn.com/fact-table-vs-dimension-table-article

![image](https://github.com/user-attachments/assets/30ad8e50-a778-45c1-92b8-5b037d214470)



