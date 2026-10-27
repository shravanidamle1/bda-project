# Student Performance Analysis using Apache Spark and HDFS

**BDA Project**

**Team**

* Harshita Kumar (B1-05)
* Shravani Damle (B1-16)

## Overview

This project analyses the Students Performance dataset (1000 students) with a big data pipeline built on Hadoop HDFS and Apache Spark. The processed results are shown in an interactive dashboard.

**Pipeline:** Dataset → HDFS → Apache Spark (DataFrame + Spark SQL) → Results saved back to HDFS → Website dashboard

## Live Dashboard

https://shravanidamle1.github.io/bda-project/

## Run the Notebook in Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shravanidamle1/bda-project/blob/main/BDA_PROJECT_StudentsPerformance_Website.ipynb)

Run all cells in order. When prompted, upload `StudentsPerformance.csv`.

## Dataset

`StudentsPerformance.csv` has 1000 rows and 8 columns:

|Column|Description|
|-|-|
|gender|Student gender|
|race/ethnicity|Group A to E|
|parental level of education|Highest education of the parents|
|lunch|standard or free/reduced|
|test preparation course|none or completed|
|math score|0 to 100|
|reading score|0 to 100|
|writing score|0 to 100|

## What the Project Does

1. Sets up a single-node HDFS inside Colab
2. Uploads the dataset to HDFS and loads it into a Spark DataFrame
3. Cleans the data (missing values, duplicates)
4. Adds features: average score, performance level, pass/fail
5. Runs group-wise analysis by gender, lunch, test prep, parental education and race
6. Runs Spark SQL queries
7. Saves the results back to HDFS (Parquet and CSV)
8. Shows the results in a web dashboard

## Run the Dashboard Locally

```bash
python serve.py
```

Then open http://localhost:8000

## Repository Structure

```
├── index.html                                      # Dashboard (GitHub Pages)
├── serve.py                                        # Local web server
├── BDA\\\_PROJECT\\\_StudentsPerformance\\\_Website.ipynb   # Spark + HDFS notebook
├── StudentsPerformance.csv                         # Dataset
└── README.md
```

## Technologies

Apache Spark (PySpark), Hadoop HDFS 3.3.6, Spark SQL, Python, Pandas, Matplotlib, HTML/CSS/JavaScript, GitHub Pages

