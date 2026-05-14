This repository contains the full implementation for the NorthStar Urban Mobility and Logistics coursework project for the Databases and Analytics module. It demonstrates how SQL in R, R analytics, Python data processing, and MongoDB Atlas can be combined to analyse operational performance and design an appropriate data architecture.

Repository structure
DATABASE/
Raw and intermediate database-related assets used during analysis (e.g. original CSVs or database exports).

northstar_cleaned_data/
Cleaned and standardised CSV files created during the data preparation phase. These are the datasets used by the notebooks for analysis and modelling.

01_sql_in_r.ipynb
Uses SQL within R (via sqldf and RSQLite) to query structured data such as deliveries, orders, customers and complaints. Focus areas:

Delivery status distribution

Delivery duration calculations

Complaints linked to delivery outcomes

Driver performance and data inconsistencies

02_r_analytics.ipynb
Performs statistical analysis and visualisation in R using ggplot2. Key charts:

Distribution of delivery duration

Delivery duration by driver

Relationship between route overrides and duration

Orders by priority level

Missing proof of delivery analysis

03_python_analysis.ipynb
Uses Python (pandas and related libraries) for deeper data processing and cross-dataset analysis. Main tasks:

Loading and cleaning operational datasets

Merging deliveries, drivers, vehicles, incidents and cost data

Investigating driver performance, vehicle condition, incidents, route overrides and cost efficiency

04_Mongo_db.ipynb
Implements a MongoDB Atlas NoSQL database using PyMongo. The notebook:

Connects to a MongoDB Atlas cluster

Creates deliveries, complaints and incidents collections

Inserts sample documents with nested structures

Demonstrates CRUD operations and an aggregation pipeline

Adds indexes and uses explain() to evaluate query performance

README.md
Project overview, file descriptions and guidance for running the notebooks.

How to run the notebooks
Clone this repository to your local machine or open it in Google Colab.

Make sure the northstar_cleaned_data folder is available in the same directory as the notebooks.

For R notebooks (01_sql_in_r.ipynb, 02_r_analytics.ipynb), install required R packages such as DBI, RSQLite, sqldf and ggplot2 in the Colab R runtime.

For Python notebooks (03_python_analysis.ipynb, 04_Mongo_db.ipynb), install dependencies such as pandas and pymongo as needed.

For 04_Mongo_db.ipynb, update the MongoDB Atlas connection URI to your own credentials before running any cells that connect to the cluster.

Purpose
This repository supports the written report by providing reproducible code and datasets for:

Identifying operational inefficiencies in NorthStar’s delivery network

Demonstrating the use of SQL in R, R analytics, Python data processing and MongoDB

Showing practical examples of query optimisation and NoSQL database design in a real-world style case study
