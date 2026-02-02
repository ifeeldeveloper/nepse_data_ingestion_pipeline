# NEPSE Data Ingestion Pipeline

## Overview
This project implements a Python-based data ingestion pipeline that processes daily NEPSE (Nepal Stock Exchange) CSV files and consolidates them into a single, structured dataset. The cleaned data is then stored in an SQLite database for efficient querying and analysis.

## Problem Statement
Develop a Python program using Pandas and SQLAlchemy to read multiple daily NEPSE CSV files from a directory, merge them into a unified DataFrame, eliminate duplicated serial numbers, generate a continuous and unique `S.No` using the DataFrame index, extract trading dates from file names, and persist the processed data into an SQLite database table.

## Key Features
- Reads multiple daily NEPSE CSV files automatically from a folder
- Merges all files into a single Pandas DataFrame
- Removes duplicated serial numbers (`S.No`) from daily files
- Generates a clean, continuous serial number using DataFrame index
- Extracts `trade_date` from file names
- Stores the final dataset into an SQLite database using SQLAlchemy

## Tech Stack
- Python
- Pandas
- SQLAlchemy
- SQLite


## How It Works
1. All daily NEPSE CSV files are read from the specified directory.
2. The data from each file is appended into a list of DataFrames.
3. All DataFrames are concatenated into a single DataFrame.
4. Duplicate serial numbers are removed and replaced with a continuous index-based `S.No`.
5. A `trade_date` column is derived from each file name.
6. The cleaned data is loaded into the SQLite table `Nepse_Data`.


