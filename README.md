# AWS Elastic Map Reduce

## Table of Contents

- [Description](#description)
- [Code-Flow](#code-flow)
- [Module-Explanation](#module-explanation)
- [Usage](#usage)
- [Architecture](#architecture)
- [Future-Development](#future-development)
## Description
This project demonstrates the use of Amazon Elastic Map Reduce (EMR) for processing large datasets using Apache Spark. It includes a Spark script for ETL (Extract, Transform, Load) operations, AWS command line instructions for setting up and managing the EMR cluster, and a dataset for testing and demonstration purposes.

## Code-Flow
The project is structured in a way that AWS Commands and Python scripts works together to Extract, Transform, Load the input data.

## Project Structure
- `spark-etl.py`: The main Spark script used for ETL operations.
- `commands.py`: Scripts for AWS EMR cluster setup and management.
- `data/`: Directory containing the dataset used for the ETL process.

## Module-Explanation

## Spark Script
The `spark-etl.py` is a Python script that uses Apache Spark to perform ETL operations. It reads data from an input directory, processes it by adding a timestamp, and writes the result to an output directory in Parquet format.

### Usage
To run the script, use the following command:
```
spark-submit spark-etl.py [s3-input-folder] [s3-output-folder]
```
Replace `[s3-input-folder]` with the path to the input data directory and `[s3-output-folder]` with the path where you want to save the output.

## AWS Commands
The `commands.py` directory contains detailed instructions and necessary scripts to set up and manage an AWS EMR cluster. This includes steps for creating an EMR cluster, configuring necessary services, and submitting Spark jobs.

## Data
The `data/` directory contains the dataset used for the ETL process. This dataset is a sample that represents the type of data the Spark script is designed to process.

## Architecture
![Architecture.png](assets%2FArchitecture.png)

## Future-Development

1) Automation Codeflow - To automate the codeflow process to continuously check for input data and process and perform ETL operations.

2) Large Datasets - To make use of large and unstructured data to perform ETL Operations.
