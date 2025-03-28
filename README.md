# data-analyst-francis
Overview of my Portfolio
Dataset: Workforce Pay Rates and Gender for the City of Vancouver from 2019 to 2023
# Portfolio Overview: To describes the processes of analyzing Workforce Pay Rates and Gender data from the City of Vancouver implemented through AWS Cloud Computing services

My Overall DAP Design for Data Ingestion, Profiling, Cleaning, Cataloging and Summarization:

# ![image](https://github.com/user-attachments/assets/04c0f0f5-2a69-4541-b98c-d455dca9cb54)

My Data Analytic Platform Design for Data Analysis to Data Monitoring and Control

# ![image](https://github.com/user-attachments/assets/4ecf5f39-ad85-41e6-8fa3-67492887d281)


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

I created database on AWS Glue:
# ![image](https://github.com/user-attachments/assets/7742a3a9-6012-4f96-8fc0-f67e1acce86a)

I also performed ETL job and summarization using AWS Glue with pipeline shown below:
# ![image](https://github.com/user-attachments/assets/f70d20c9-4501-49fa-a88a-47d612071961)


Insights and iNTERPRETATION OF SUMMARIZED RESULTS
1. The pay gap between male and female Genders staff at CUPE 15 'Admin Support Ia' 
•	In 2019: The salary data from 2019 shows that male hourly rates averaged $32.00 while females received $29.00 as their average pay (Calculated from provided dataset using average of min/max). Pay Gap = 9.375%.
•	In 2022: The analysis shows that male staff earn $38.82 per hour while female employees earn $26.5 (under the assumption that there is no pay difference in administrative positions) leading to a -46.49% pay gap in their favor (females receive higher pay).
Interpretation: Rates paid to male employees were higher than female rates in 2019 yet female employees earned more than males during 2022. Further analysis needs to determine if the data composition changed because it likely affected this shift.
2. Gender Representation in 'Exempt' vs 'CUPE 15' positions (Focus on Manager 1 role)
•	2019 (Exempt Manager 1): 36 Females, 31 Males (54% Female)
•	2022 (Exempt Manager 1): No information
2023 (Exempt Manager 1): 40 Females, 26 Males (61% Female)
•	In 2019: The operational support workforce of CUPE 15 shows 9 female workers out of 34 (26.5 %) while 25 male employees make up the remaining staff in 2019.
No data can be found about the gender distribution among 2022 Operational Support AI personnel (CUPE 15 - closest available is Operational Support AI).
The current workforce distribution reveals 5 female and 14 male staff at 'Operational Support IV' (CUPE 15) positions in 2023 (26.3% Female).
Interpretation: The 'Exempt' 'Manager 1' positions demonstrate nearly equal gender participation through their increased female workforce numbers over the years. The 'CUPE 15' 'Operational Support' workforce consists predominantly of male staff members as their gender distribution shows no signs of shifting.
3. 'Senior Exempt' Pay (Illustrative due to wide range):
•	2019: Minimum $78.95, Maximum $96.72 (Only for Legal 3). The job distribution shows nearly equal participation from male and female colleagues who work together at the organization (13 females and 18 males). Average $87.83.
•	2022: Male demographic dominates the "multiple job classifications" roles in 2022 since they comprise 17 workers against 9 female employees. The pay scale varies from $70.94 to $165.31. Average $118.12.
•	In 2023: the General Manager 2 position spans between $99.6 at the entry level to $148.74 at the top level with most positions held by male employees (9 females and 3 males). Average $124.17.

# Tools and Technologies:

     * AWS S3 Transform Bucket
     * AWS Glue Databrew
     * AWS Glue
     * AWS Crawler
# Deliverables:    
     * The Gaps in Workforce Pay Rates are Complex
     * How the Data is Represented Matters
     * Senior Job Officers Command Higher Pay Rates
     * Cleaned & Transformed Dataset in S3, partitioned by year or classification (if needed).
     * Wrangling Report documenting recipes and transformations saved in the User and Systems folders in the Transformed and Curated S3 Storage Buckets

### DATA QUALITY CONTROL
# Project Description: Data Quality Control (DQC) ensures the dataset remains accurate, complete, consistent, and reliable. This process is vital to maintaining trust and usability in the City of Vancouver’s workforce data, and this happens by setting monitoring and controlling plans in place that is automated.
# Project Title: Monitoring and Controlling of Workforce Pay Rates and Gender Dataset DAP Design for the City of Vancouver
# Objective: The main objective of data monitoring is to ensure that the system continuously monitors activities of the dataset while identifying irregularities in security by triggering warning signals for potential threats.
# Background: After completion of Data Wrangling process and with multiple job classifications and an evolving workforce, the City of Vancouver’s pay-rate dataset can quickly become inconsistent or outdated. Routine checks are essential to validate completeness, uniqueness, and freshness.
# Scope: The project will focus on the following key areas:
•	Data Validation: Implementing validation rules and checks to ensure data integrity for the City of Vancouver.
•	Monitoring and Reporting: Establishing ongoing monitoring processes and dashboards to track data quality metrics.
•	Training and Awareness: Creating training programs for staff on data quality best practices.
# Methodology:
     1. Current State Assessment: 
Recall that I had evaluated the raw, cleaned, and summarized datasets for recurring errors (e.g., large outlier values in the Maximum Hourly Rate for certain job classifications) after my thorough data profiling and cleaning operation with 23 changes made as shown in the data wrangling picture above, with cleaned datasets currenlty in transformed buckets and summarized datasets now in the curated S3 buckets.
     2-	Data Profiling:
I used data profiling tools to assess the quality of identified datasets, focusing on completeness, uniqueness, validity, consistency, and accuracy.
I also documented findings to highlight areas requiring immediate attention.
     3. Establish Data Quality Metrics:
•	I created a dashboard with the name: workforce-prs-MCR-fra

•	I initiated 3 monitoring actions:
i.	Line graph in BucketSizeBytes of S3 raw bucket service used
ii.	Line graph of ResourceUsage from AWS Glue service used
iii.	Bar graph showing joint BucketSizeBytes analysis of the raw, transform and curated buckets
•	I also Implemented Controlling Actions by installing Billing Alarm: The aim of this is to control user activities by setting up an alarm that keeps us posted whenever we are starting to exceed certain threshold.
Image showing how I set up Monitoring and Controlling Dashboard on AWS CloudWatch
# ![image](https://github.com/user-attachments/assets/29b43079-0c6e-4864-b8bc-f0bbbb77334c)

Results of Passed Quality Check
# ![image](https://github.com/user-attachments/assets/8ab3bd74-4bba-4af9-9c93-567a4151a195)

Results of Failed Quality Checks
# ![image](https://github.com/user-attachments/assets/9ae09b15-1683-4f76-842c-f339ed5b516a)

4. I Established Data Quality Metrics
* Completeness: e.g., 95% of rows must have valid numeric hourly pay.
* Uniqueness: e.g., minimal duplication in classification-year entries.
* Validity: e.g., no negative pay rates.

5-	Validation Rules and Procedures:
* Automated transformations to remove or correct invalid data.
* I did Partitioning in S3 into “Passed” and “Failed” folders based on thresholds.
Image showing Event History for the COV Payrates and Sex Dataset from AWS CloudTrail Solution
# ![image](https://github.com/user-attachments/assets/e798ec0e-4002-4d77-a7bc-ac71c11c44b0)

Image showing an Overview of User Activity on AWS CloudTrail Service 
# ![image](https://github.com/user-attachments/assets/a0f68152-7957-4237-a060-8430704daa0a)

# Deliverables: Here are the key phases completed:
Key phases completed:
1.	Data Analysis: achieved business intelligence at five stages through the utilization of S3, AWS Glue and Athena to perform descriptive, diagnostic, predictive, prescriptive and causal analysis. The business got answers to actual business questions about workforce changes and gender pay differences and salary projections by running SQL queries on the database.

2.	Data Security: Pay and gender data protection was achieved through the implementation of AWS KMS, IAM roles, bucket replication and encryption policies.

3.	Data Governance: The AWS S3 quality-check pipelines and AWS Glue Data Quality rules performed Data Governance functions through standard assessments of data completeness and uniqueness and freshness.

4.	Data Monitoring: employed CloudWatch together with SNS and CloudTrail to create performance dashboards, execution time monitoring functions, billing alerts, and security operation control through activity tracking.

# Recommendations for the City of Vancouver:
 * Implement the Current DAP Solution Design
 * Improve Data Freshness and Diversity
 * Strengthen Access and Encryption Policies
 * Monitoring & Alerts should be made Operational
 * Increase Analytical Capabilities to link with other platforms

# Conclusion
The workforce pay rates and sex clearly has undergone processes from data ingestion to monitoring and control, and various quality issues have been identified and fixed. If all the recommended actions and properly implemented by the City of Vancouver, not only will the quality of data received improve greatly, but also, there would be outstanding closure in pay gaps across all job classificaions before end of Q4 2030.


