# Uber Data Engineering Project

![Uber Logo](./assets/uber%20logo.jpg)

## Introduction

This is my personal project in order to further amplify my understanding towards data engineering especially in using ETL pipeline thanks to 
Darshil Parmar Tutorial on Youtube. The tools that will be used on this project are **Jupyter Notebook, GCP Storage, Python, Compute Instance, Mage AI, BigQuery, and Looker Studio.**

## Dataset Used

We will use NYC TLC Trip Record dataset for this project. The dataset contains yellow and green taxi trip records which include fields that capture pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

The dataset used for this project can be found here: https://github.com/lodaogos/uber-data-engineering-project/blob/main/data/uber_data.csv

More information about the dataset can be found here:
1. TLC Website: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
2. TLC Data Dictionary: https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf

## Data Modelling Using draw.io

In order to use our dataset efficiently, we can first create a data model by dividing the data into dimension table and fact table. In data warehousing, a dimension table is a database table that stores attributes describing the facts in a fact table. Fact table usually contains the FK of a dimension table. In addition to these foreign keys, the fact table also contains measures or facts, which are often numeric and used for analysis. You can read more about it here: https://www.simplilearn.com/fact-table-vs-dimension-table-article

![image](https://github.com/user-attachments/assets/30ad8e50-a778-45c1-92b8-5b037d214470)

## Transformation Code in Jupyter Notebook

I wrote the code for transformation in [jupyter notebook](https://github.com/lodaogos/uber-data-engineering-project/blob/main/uber_transform.ipynb). This code clean the data and transform it into similar structure with the fact table we have created before.

![image](https://github.com/user-attachments/assets/166e3c59-e176-4c06-869f-29996ec65ff3)

## Using Google Cloud Bucket

I uploaded the csv data into google cloud bucket

![image](https://github.com/user-attachments/assets/a5bab96d-ab78-44ad-8e98-c058d73fe1fb)

## Using Google Compute Engine To Run mage.ai

I created a VM instance using the google cloud compute engine. In the VM i installed python and then followed the documentation on [mage.ai](https://github.com/mage-ai/mage-ai?tab=readme-ov-file#%EF%B8%8F-quick-start) to run mage.ai on the instance. I also configured the VM in a way so that i can access it from the browser.

```
# Command to run the VM and install mage.ai

# Install the dependecies
sudo apt-get update
sudo apt-get install python3-distutils
sudo apt-get install python3-apt

# Install and create virtual env
sudo pip3 install virtualenv
python3 -m venv .venv
source .venv/bin/activate

# Install mage.ai
sudo pip3 install mage-ai

# Install google-cloud dependecies
sudo pip3 install pandas
sudo pip3 install google-cloud
sudo pip3 install google-cloud-bigquery

# Start mage
mage start uber_de_project
```

![image](https://github.com/user-attachments/assets/f50abf24-56d2-4d69-9b7a-61f63a7d49ad)

![image](https://github.com/user-attachments/assets/ad125b29-11e4-480e-92a1-5b96d33c42d1)


## Using mage.ai To Do ETL Process

I then write some code in mage.ai to do some ETL process of the data.

![image](https://github.com/user-attachments/assets/76482412-505a-4d19-8ace-984b3eb9dfac)

## Data Succesfully Loaded Into BigQuery

We can check if the data succesfully loaded into the BigQuery by trying to query it.
![image](https://github.com/user-attachments/assets/0deceae5-53ed-4427-9aad-4c7c2a27ef98)

## Creating A Dashboard Using Looker Studio

After finish loading the data into BigQuery, we can connect the data from BigQuery into looker studio to build a [dashboard](https://lookerstudio.google.com/reporting/949c81c6-5044-45f0-8791-7a2f6abcacbe).

![image](https://github.com/user-attachments/assets/58765ed9-cb24-4e25-8cb3-90df98ee3c29)











