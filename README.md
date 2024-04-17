# This project delivers a detailed data pipeline system for extracting, transforming, and loading Reddit data into a Redshift database. It utilizes various tools such as Apache Airflow, Celery, PostgreSQL, Amazon S3, AWS Glue, Amazon Athena, and Amazon Redshift.

# Table of Contents
- Overview
- Architecture
- Prerequisites
- System Setup
- Overview

## The purpose of this pipeline is to:

- Extract Reddit data using its API.
- Deposit the raw data into an S3 bucket via Airflow.
- Process the data using AWS Glue and Amazon Athena.
- Import the processed data into Amazon Redshift for analysis and querying.

Reddit API: Initial data source.
Apache Airflow & Celery: Coordinates and manages the ETL tasks.
PostgreSQL: Provides temporary storage and manages metadata.
Amazon S3: Stores the raw data.
AWS Glue: Handles data cataloging and ETL operations.
Amazon Athena: Executes SQL-based transformations.
Amazon Redshift: Used for data storage and analytics.

## Prerequisites

- An AWS account with the necessary permissions for S3, Glue, Athena, and Redshift.
- Credentials for the Reddit API.
- Docker installed.
- Python version 3.9 or later.

Download the repository
'git clone https://github.com/airscholar/RedditDataEngineering.git'

Set up a virtual environment.
'python3 -m venv venv'

Activate the virtual environment.
'source venv/bin/activate'

Install required packages.
'pip install -r requirements.txt'

Update the configuration and credentials files.
'mv config/config.conf.example config/config.conf'

Initialize the Docker containers.
'docker-compose up -d'
Access the Airflow web interface.
'open http://localhost:8080'

