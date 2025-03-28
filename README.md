# data-analyst-francis
Overview of my Portfolio
Dataset: Workforce Pay Rates and Gender for the City of Vancouver from 2019 to 2023
# Portfolio Overview: To describes the processes of analyzing Workforce Pay Rates and Gender data from the City of Vancouver implemented through AWS Cloud Computing services

### EXPLORATORY DATA ANALYSIS
# Project Description: Performing EDA on Workforce Pay Rates and Gender Dataset.
# Project Title: Reviewing Equity in Workforce Pay: An Exploratory Data Analysis
# Objective: This main aim of this analysis is to understand patterns and trends and extract insights about salary distribution and workforce categories and gender equality from the City of Vancouver Workforce Pay Rates and Gender dataset.
# Dataset: The components of the dataset includes:
      * Year (2019 -  2023)
      * Exempt/Union status
      * Classification and position titles
      * Hourly pay rates (Minimum, Maximum)
      * Gender or Sex demographics (Female, Male, Total)
# Methodology: 
1. Data Collection and Preparation
     * Ingested the CSV dataset into Amazon S3 (Raw bucket).
     * Ensured the CSV file was accessible for further profiling and cleaning (see Figure 1 below).
**Figure 1**: Downloaded Workforce Dataset (CSV) in S3
# ![image](https://github.com/user-attachments/assets/30e00950-07c7-4ac4-9c45-a4259be68840)
Source: Francis’ Project – City of Vancouver

Then I saved the downloaded document in AWS Raw S3  Bucket as shown in the image below:
# ![image](https://github.com/user-attachments/assets/02db89fb-580a-48d7-ba0e-583f9191cbdb)

2. Initial ProfilinG
Used Excel and to generate statistical visualizations on data completeness, duplicates, min/max values, and potential outliers. 
# ![image](https://github.com/user-attachments/assets/ce26eaf7-8490-45e7-97da-040900376b77)

3. Descriptive Summaries
     * Calculated summary statistics (mean, median, mode) for the numerical columns (Minimum and Maximum Hourly Rate, Female, Male, Total).
     * Counted the frequency distribution of classification types and union/exempt categories.
4. Data Visualization
* Created basic charts (box plots, bar charts) to reveal distributions of hourly rates and how they differ across classification types and years.
# ![image](https://github.com/user-attachments/assets/95683203-070c-4fb9-9d9a-f775baf92814)
# ![image](https://github.com/user-attachments/assets/3dff2b98-37e5-4451-99d1-c69eaf18c667)

5-	Insights and Findings:
     * Summarize the findings based on data visualizations and statistical analyses
     * Highlight of notable trends and patterns (e.g., women and children had higher survival rates, first-class passengers had a significant survival advantage).
# ![image](https://github.com/user-attachments/assets/af0c9ee5-42db-44c6-8759-1f7ceaadd6d2)
# ![image](https://github.com/user-attachments/assets/0483e0de-0680-4d2e-ba7d-f3ee5e3cb467)

# Tools and Technologies:
     * AWS S3 for data ingestion
     * AWS Glue DataBrew for profiling and cleaning
     * Microsoft Excel CSV file for exploratory charts
     * City of Vancouver Website

### DESCRIPTIVE ANALYSIS
# Project Description: Descriptive Analysis aims to answer the question “What happened?” by summarizing historical pay data and highlighting trends or patterns in purchasing or workforce contexts. Here, we apply descriptive analysis to further quantify and categorize the City of Vancouver workforce pay data, examining total staff counts, distribution by classification, and year-over-year changes.
# Project Title: Descriptive Analytics of Workforce Pay Structures at the City of Vancouver
# Objective: My objective here was to extract patterns (such as trends, seasonality, frequency of occurrence, correlations, clusters, anomalies etc.) and with this, I would need AWS Athena service to populate queries and tables using the SQL. 
# Dataset: I used the same dataset from the City of Vancouver, focusing on the aggregated staff counts (female, male, total), pay rate columns, and the job classifications within either exempt or union categories.
# Methodology: 
     1. Data Ingestion and Cleaning
          I built upon the cleaned data from the EDA phase, used the refined columns (Year, ExemptOrUnion, Classification, Min/Max Hourly Rate, Female, Male, Total) for descriptive calculations.
     2. Statistical Summaries
          I did descriptive summary on excel
# ![image](https://github.com/user-attachments/assets/67f2584a-b1e1-4be0-ad6b-311c2c869a67)
Distribution of hourly wages in minimum and maximum pay
# ![image](https://github.com/user-attachments/assets/ff75997b-8ef7-447a-ae27-a5b0dc48ccd3)

I prepared the lcoation of my queried dataset in the curated S3 bucket
# ![image](https://github.com/user-attachments/assets/12fd1a4b-d711-4c31-b6fb-5ec4bd59556c)
      3. visual Representation of my Descriptive Business Questions (these were done on AWS Athena for SQL codes)
A. What is the average hourly rate of pay (Minimum and Maximum) per year?
# ![image](https://github.com/user-attachments/assets/1c525471-675d-4e10-85f3-99ba75ba0900)

B. What is the number of Staff members per year?
# ![image](https://github.com/user-attachments/assets/47dd80da-79aa-47cf-8563-bb80c0ee8149)

      4. Insights and Findings
A. The SQL query to business question 1 shows that the overall change in pay rates over a 5-year period, with the least average minimum hourly rate being over $35 in 2019 and the highest average hourly rate occurring in 2023, showing an upward trend.
B. The rise in workforce in 2020 witnessed a decrease in 2021 from 3,248 to 3,157. In general, 2023 workforce count (3,301) has been the highest in the last 5 years.

     5. Continued efforts need to be combined to ensure that wage gap is bridged across genders and different job classifications.

# Tools and Technologies:
     * SQL Query Editor
     * AWS Athena
     * AWS Glue Databrew
     * AWS Curated S3 Storage bucket

# Deliverables: I was able to show:
     * Detailed Descriptive Report: Summarizing distribution metrics and year-over-year trends
     * Visual Representation of SQL Queries that answered my business questions

### DIAGNOSTIC ANALYSIS
# Project Description: This answered the question “Why did it happen?” by looking into relationships between variables—such as classification, gender representation, and year-to-year pay changes—and identifying possible causes for observed trends.
# Project Title: Investigating Differences in Pay Distribution in the City of Vancouver
# Objective: This analysis enabled me to find patterns of change across a single column from our data of workforce-pay-rates-and-gender from the City of Vancouver from 2019 to 2023. This will be implemented by answering more business questions that will be solved using Athena and SQL.
# Background: A notable finding during EDA and Descriptive Analysis was that the large gap existed in the maximum hourly rates in senior-level or exempt positions. Also, the workforce composition in certain operational or support roles was found to be largely dominated by male gender.
# Dataset: I used the previous workforce-pay-rates-and-gender dataset already uploaded from the AWS Glue Databrew to AWS Athena for querying using SQL
# Methodology: 
1. I asked 1 diagbistic business question:
Business Question: Which of the Job Classifications record the highest pay variations/differences?
2. visual Representation of my Descriptive Business Questions 
# ![image](https://github.com/user-attachments/assets/7a407cc1-e4cb-4a00-acdc-b3b36a01ce6b)
3. Insights and Findings
Clearly, there is a variation in pay rates with the highest (over $139/hour) being multiple classifications while legal 3 earns only $26.44 per hour. However, we are not sure if the large difference is due to experience level or scales of job tasks assigned.
# Tools and Technologies:
     * Amazon Athena for SQL-based query runs
     * AWS Glue: to populate data tables into the AWS Athena for further processing
# Deliverables:
I made a brief Diagnostic Report explaining the top factors that influence pay gaps from project 2
# Timeline: 
This data was collected across a 5-year period (from 2019 to 2023).

### Data Wrangling
# Project Description: I used AWS Glue Databrew to Profile (identify data quality issues in the dataset) and clean the data, while I used AWS Glue to perform data cataloging and data summarization using Extract, Transform and Load (ETL) Operation. Generally, this shows the process of cleaning, transforming, and consolidating data to ensure it is ready for downstream analysis and reporting.
# Project Title: Profiling, Cleaning and SUmmarizing Workforce pay rate and gender dataset for the City of Vancouver Workforce Dataset for Analysis
# Objective: To identify all data quality issues, rectify all data quality issues—missing columns, incorrect data types, inconsistent classification labels—and produce a summarized and clean, ready-to-analyze dataset that can be seamlessly passed into analytics tools.
# Background: Data dowbnloaded has data quality issues identified
# Dataset: Workforce pay rates and gender dataset earlier identified
# Methodology: 
1. Data Profiling: Profiling my dataset is the process of assessing, analyzing and understanding the issues, content, structure and quality of my dataset to ensure it is good enough for cleaning. That is, in this phase, I will critically review my dataset to understand the present quality and understand, which means it is a data preparation tool that helps me to gain more insights into my data quality and readiness to be cleaned.
   Data was Ingested from Transform bucket on S3 storage
# ![image](https://github.com/user-attachments/assets/a5bedd01-772a-48c3-aa7c-4004d7ad1957)

Image of Profiled Dataset on AWS Glue Databrew
# ![image](https://github.com/user-attachments/assets/20e1c373-99e8-42eb-9335-b13e68bc1336)

Result of profiled dataset
# ![image](https://github.com/user-attachments/assets/92840dfe-59c3-4003-bc84-695c4d058fc5)

* Data Cleaning:
Congested Workforce data:
![image](https://github.com/user-attachments/assets/c3ed5e52-420c-44f1-82f4-869f74356365)

23 cleaning operations performed
# ![image](https://github.com/user-attachments/assets/868497c5-3ba9-44bb-99d8-9b667d766732)

Changed data type
# ![image](https://github.com/user-attachments/assets/da7c0475-51cf-483a-b4b1-54dc086279e6)
 Cleaned User data
# ![image](https://github.com/user-attachments/assets/8c95d446-e8e0-45e3-a8b9-4da663fcae04)

Cleaned System data
# ![image](https://github.com/user-attachments/assets/0725d99c-55e7-4399-ab9f-f16a02efa6dc)

Insights:
The Data Quality Issues I Identified during Data profiling Process:
a)	During data profiling, I observed that, though there were 540 rows, the dataset are all in one column instead of being in different columns and they are separated by semi-colon (;) as shown in Figure 11 above, which means I need to split them into different columns before I can do cataloging and summarization. 
Apart from the raw data being unstructured in 1 column, other noted data issues were identified:
b)	Outlier values in the Minimum hourly rate, Maximum hourly rate, Female, Male and Total categories
c)	Inconsistent Values in the”” “Exempt/Union” category, because more categories fall under these two as compared to very few counts for other categories.
d)	Cross Field Issue (especially for the Female, Male and Total categories). This also occurs for the hourly rates because the minimum hourly rates ought to be less than or equal to the maximum hourly rates.
e)	Redundant Values in the Data category, containing only aggregated data
f)	Granularity Issue: This is obvious in the Female; Male and Total Categories. This issue also affects the Classification Category
g)	Invalid Values: Because “Multiple Classification” in itself is not a group and “position title” being a column header is not a specific position
h)	Outdated Values: Since the dataset is from 2019 to 2023, I am curious about why there was no record for 2024 or 2025, because so many changes could have occurred to our results.

# Tools and Technologies:

     * AWS S3 Transform Bucket
     * AWS Glue Databrew
     * AWS Glue
     * AWS Crawler
# Deliverables:
# Timeline:

### Data Quality Control
# Project Description: 
# Project Title:
# Objective:
# Background:
# Scope:
# Methodology:
# Deliverables:
# Timeline:


