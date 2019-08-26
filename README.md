# BigDataApacheSpark-ChurnOrNot

## Installation
The following was used for the environment setup:

* Python 3.5
* PySpark SQL
* PySpark ML
## Project Motivation
This project attempts to solve big data problems using pyspark. It answers some questions based on data exploration using both spark sql 
and dataframe. Also features were engineered features and finally a pipeline is built for the model. A small subset of the sparkify dataset in json format was used.

For a fictional music streaming service (Sparkify), we are interested in seeing if we can predict which users are at risk of 
cancelling their service. The goal is to identify these users before they leave so they can hypothetically receive discounts and 
incentives to stay.

## File Descriptions
* BigDataApacheSpark-ChurnOrNot.ipynb
* README.md

## Feature Engineering
During feature engineering, I applied the following transformations to the data:

String Indexer:

Gender_indexer (inputCol="gender")
User_indexer (inputCol="userAgent")
Page_indexer (inputCol="page")
indexer (inputCol="Churn")
One Hot Encoding:

Gender_encoder (inputCol='Gender_Index')
User_encoder (inputCol='User_Index')
Page_encoder (inputCol='Page_Index')
Vector Assembler:

assembler (inputCols=["Gender_Vec", "User_Vec", "Page_Vec", "status"])
## Acknowledgements
The data was taken from the following (https://s3.amazonaws.com/video.udacity-data.com/topher/2018/December/5c1d6681_medium-sparkify-event-data/medium-sparkify-event-data.json)
