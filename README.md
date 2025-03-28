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

# Tools and Technologies:
# Deliverables:
# Timeline:


### Data Wrangling
# Project Description: 
# Project Title:
# Objective:
# Background:
# Dataset:
# Methodology:
# Tools and Technologies:
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


