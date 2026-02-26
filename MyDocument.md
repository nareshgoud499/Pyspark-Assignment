MyDocument.md

NYC Jobs Data Engineering & Analytics Project

------------------------------------------------------------------------

1. Project Overview

This project analyzes the City of New York’s job postings dataset using
PySpark in a distributed data processing environment (Google Colab Spark
setup).

Goals: - Perform detailed data exploration and profiling - Extract
business insights through KPIs - Apply data cleaning and transformation
techniques - Implement feature engineering - Store processed data for
downstream use - Propose deployment and triggering strategies

------------------------------------------------------------------------

2. Dataset Description

The dataset contains active job postings published on the City of New
York official jobs portal.

Key Columns Include: - Job ID - Agency - Business Title - Civil Service
Title - Job Category - Salary Range From - Salary Range To - Salary
Frequency - Posting Date - Preferred Skills - Minimum Qualification
Requirements - Residency Requirement - Work Location

------------------------------------------------------------------------

3. Data Exploration & Profiling

Column Classification

Numerical Columns: - Salary Range From - Salary Range To - # Of
Positions - Level - Title Code No

Categorical Columns: - Agency - Posting Type - Business Title - Civil
Service Title - Job Category - Full-Time/Part-Time indicator - Salary
Frequency - Work Location - Residency Requirement

Date Columns: - Posting Date - Post Until - Posting Updated - Process
Date

------------------------------------------------------------------------

4. KPIs Implemented

1.  Top 10 Job Categories by Posting Count
2.  Salary Distribution per Job Category
3.  Correlation Between Higher Degree and Salary
4.  Highest Salary per Agency
5.  Average Salary per Agency (Last 2 Years)
6.  Highest Paid Skills

------------------------------------------------------------------------

5. Data Processing

Cleaning Steps: - Removed duplicates - Handled null salary values -
Standardized date formats - Dropped irrelevant columns

Feature Engineering: 1. Average Salary (midpoint of salary range) 2.
Salary Range Width 3. Degree Requirement Indicator 4. Posting Year

Feature Removal: - Recruitment Contact - To Apply - Additional
Information

------------------------------------------------------------------------

6. Data Storage

Processed dataset saved as: processed_nyc_jobs.csv

------------------------------------------------------------------------

7. Test Cases

-   Dataset not empty validation
-   Average Salary column existence check
-   Negative salary validation
-   Null handling verification

------------------------------------------------------------------------

8. Deployment Proposal

Option 1: Batch Pipeline Deployment (AWS EMR / Databricks) Option 2:
Scheduled Workflow (Apache Airflow) Option 3: REST API using FastAPI

------------------------------------------------------------------------

9. Trigger Strategy

-   Cron-based scheduler
-   Airflow DAG
-   CI/CD pipeline
-   Cloud function trigger

------------------------------------------------------------------------

10. Learnings

-   Spark Window functions for ranking
-   Feature engineering improves analytical insights
-   Correlation in Spark is efficient for numerical variables

------------------------------------------------------------------------

11. Challenges

-   Handling null salary values
-   Parsing degree requirements from text
-   Extracting meaningful skills from free text
-   Managing Spark memory in Colab

------------------------------------------------------------------------

12. Assumptions

-   Salary midpoint represents compensation
-   Degree detected via keyword matching
-   Preferred Skills separated by commas
-   Last 2 years calculated from current date

------------------------------------------------------------------------

13. Future Improvements

-   Advanced NLP for skill extraction
-   Salary prediction modeling
-   Interactive dashboard
-   Cloud-based distributed deployment

------------------------------------------------------------------------

Conclusion

This project demonstrates end-to-end PySpark data engineering workflow,
KPI analysis, feature engineering, scalable processing, and deployment
readiness.
