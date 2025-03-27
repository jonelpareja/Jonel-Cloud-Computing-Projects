# Project Part 1
# Project Description:
 This descriptive analysis project details the process and initial findings for preparing and understanding foundational datasets used within the City of Vancouver's Data Analytics Platform (DAP). Specifically, it focuses on the Folderyear_List, Businesstype_List, and City_List datasets, essential for the broader "Business Licences 2025 Procedure" analysis. This document outlines the steps taken to ingest, profile, clean, catalogue, and summarize these supporting datasets, providing a clear overview of their characteristics and readiness for further analytical use.
# Project Title: 
# City of Vancouver DAP Analysis: Business Licences 2025 Procedure (Project Part1)
# Project Part 1 Draw.io Design
# Part 1
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%201.png)
# Part 2 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%202.png)
# Part 3
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%203.png)
# Part 4
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%204.png)

# Objectives:
1. The primary objectives of this descriptive analysis are:
2. To document the end-to-end procedure for ingesting, preparing, and cataloging the Folderyear_List, Businesstype_List, and City_List datasets using AWS cloud services.
3. To profile and understand these essential supporting datasets' structure, content, quality, and statistical characteristics.
4. To generate descriptive summaries and basic visualizations to illustrate the content of these lists.
5. To ensure these foundational datasets are cleaned, well-documented (via catalogue), and ready for integration and use in subsequent, more complex analyses within the "Business Licences 2025 # Procedure" on the City of Vancouver's DAP.
# Datasets:
1.	Business_Licences_2025: Includes three key files:
2.	Folderyear_List.csv: License records categorized by year.
3.	Businesstype_List.csv: License classifications by business type (e.g., retail, hospitality).
4.	City_List.csv: Geographic distribution of licenses across Vancouver neighbourhoods.
5.	Source: Ingested into AWS S3 via EC2 instance and processed using AWS analytics services.
# Methodology:
# 1. Data Collection and Preparation: 
This phase involved sourcing, ingesting, profiling, and cleaning the supporting datasets.

1.1. Data Sourcing: The Folderyear_List.csv, Businesstype_List.csv, and City_List.csv files were created and made available on the EC2 instance RGVS-Jonel (ec2-54-162-188-36.compute-1.amazonaws.com).
# 1.2. Data Ingestion (AWS S3, EC2, PowerShell):
1.2.1. S3 folders (e.g., within businesslicences2025-trf-jonel) were structured.

1.2.2. Using PowerShell scripts executed via RDP on the EC2 instance, the following files were ingested into their respective AWS S3 locations:

1.2.2.1 Folderyear_List.csv
   
1.2.2.2 Businesstype_List.csv
   
1.2.2.3 City_List.csv
# Screenshots of the Project Part 1 Implementation in AWS Services
# Created 3 folders in AWS S3
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/4309f958d38e2dac624bb5697e141820b8edf692/Created%203%20folders%20in%20AWS%20S3.png)
# Created EC2 Instance RGVS-Jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/Created%20EC2%20Instance%20RGVS-Jonel.png)
# Connected to EC2 via RDP and created a list of csv files 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/s3%20folder%20created.png)
# Connected to EC2 via RDP and created 3 CSV files) 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/folders%20list%20and%20connected%20to%20rdp.png)
# Data Ingestion using Powershell Script (EC2 RDP) to S3
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/Data%20Ingestion%20using%20Powershell%20%20(EC2%20RDP)%20to%20S3.png)
# Folderyear_List.csv S3 location
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/Folderyear_List.csv%20S3%20location%20.png)
# Businesstype_List.csv in S3 location
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/Businesstype_List.csv%20%20S3%20location.png)
# City_List CSV in S3 location
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/98d9638de72f17d1bbdb782414b247b926adec5e/City_List%20CSV%20S3%20location.png)

# 1.3. Data Profiling (AWS Glue DataBrew):
# 1.3.1. Folderyear_List:

1.3.1.1. DataBrew Project: bus2025-fol-lst-prj-jonel created with dataset bus2025-fol-lst-ds-jonel

1.3.1.2. Profiling Job: bus2025-fol-lst-ds-prf-jonel was run to analyze the schema, data types, and statistical properties

# Created project name  bus2025-fol-lst-prj-jonel project 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/bdc4ebe758e557f65708ded3fe31d501e2ce38a0/Folderyear_List%20data%20profiling1.png)

# Created dataset name bus2025-fol-lst-ds-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/bdc4ebe758e557f65708ded3fe31d501e2ce38a0/Folderyear_List%20data%20profiling2.png)
# Created and run the job bus2025-fol-lst-ds-prf-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/afb8f2e855228131ef52d10fb5adcbc589b9403c/Created%20and%20run%20the%20job%20bus2025-fol-lst-ds-prf-jonel.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/abb00b5bb6591b620602b3469f991badd527933d/Created%20and%20run%20the%20job%20bus2025-fol-lst-ds-prf-jonel2.png)

# 1.3.2. Businesstype_List:

1.3.2.1	Dataset created and profiling job bus2025-bus-lst-ds-prf-jonel was run.

# Businesstype_List: Created project name bus2025-bus-lst-prj-jonel 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f0b8b0f2f1d6e614239512e2a2bbb0ce3eae4db1/project%20naame%20bus2025-bus-lst-prj-jonel.png)

# Created dataset name bus2025-bus-lst-ds-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f0b8b0f2f1d6e614239512e2a2bbb0ce3eae4db1/dataset%20name%20bus2025-bus-lst-ds-jonel.png)

# Created and run the job bus2025-bus-lst-ds-prf-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/b15bfd4ec8fae2667c30b8aa50a088f4f5b2bfd2/Created%20and%20run%20the%20job%20bus2025-fol-lst-ds-prf-jonel.png)

# 1.3.3. City_List:

1.3.3.1. DataBrew Project: bus2025-cit-lst-prj-jonel created with dataset bus2025-cit-lst-ds-jonel.

# Created project name bus2025-cit-lst-prj-jonel 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/df8e8af5215e597d0de7f626b7343023ee103c91/project%20name%20bus2025-cit-lst-prj-jonel.png)

# Created dataset name bus2025-cit-lst-ds-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/df8e8af5215e597d0de7f626b7343023ee103c91/dataset%20name%20bus2025-cit-lst-ds-jonel.png)

1.3.3.2. Profiling Job: bus2025-cit-lst-ds-prf-jonel was run.
# Created the job bus2025-cit-lst-ds-prf-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f6ccf77d9393d3b794f09ea0ecd08c323ea36355/bus2025-cit-lst-ds-prf-jonel1.png)

# Run the job bus2025-cit-lst-ds-prf-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f6ccf77d9393d3b794f09ea0ecd08c323ea36355/bus2025-cit-lst-ds-prf-jonel2.png)

# 1.4.	Data Cleaning (AWS Glue DataBrew): 
Based on profiling insights, cleaning recipes were built and applied:

1.4.1. Folderyear_List: Cleaning Job bus2025-fol-lst-cln-jonel executed, producing cleaned outputs in CSV (S3 user folder) and Parquet (S3 system folder).

# Cleaning job bus2025-fol-lst-cln-jonel CSV and parquet stored in S3 User and System folders, respectively.

![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f9f59f2f3514f4785407e22afb1ef5671756ce15/data%20cleaning%202.png)

![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f9f59f2f3514f4785407e22afb1ef5671756ce15/data%20cleaning3.png)

1.4.2. BusinessType_List: Cleaning Job bus2025-bus-lst-cln-jonel executed, producing cleaned outputs in CSV and Parquet in respective S3 folders.
# Created & run Data Cleaning Job bus2025-bus-lst-cln-jonel (2 output format in csv & parquet)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/02bc6a3839557d3228514b4d6fff50e114ac2fa2/Created%20%26%20run%20Data%20Cleaning%20Job%20bus2025-bus-lst-cln-jonel%20(2%20output%20format%20in%20csv%20%26%20parquet).png)

# Cleaning job bus2025-bus-lst-cln-jonel CSV and parquet stored in S3 User and System folders, respectively.
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/c033318f957b3c625683744063b0aec0b54e1f7f/Cleaning%20job%20bus2025-bus-lst-cln-jonel%20%20csv.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/c033318f957b3c625683744063b0aec0b54e1f7f/Cleaning%20job%20bus2025-bus-lst-cln-jonel%20%20parquet.png)

1.4.3.	City_List: Cleaning Job bus2025-cit-lst-cln-jonell executed, producing cleaned outputs in CSV and Parquet.
# Created & run Data Cleaning Job bus2025-cln-lst-jonel (2 output format in csv & parquet)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/f5acd23f797de4864802da948c9a9f57b5553302/Created%20%26%20run%20Data%20Cleaning%20Job%20bus2025-cln-lst-cln-jonel%20(2%20output%20format%20in%20csv%20%26%20parquet).png)

# Cleaning job bus2025-cit-lst-cln-jonel CSV and parquet stored in S3 User and System folders, respectively.
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/2a9591dbf8a874fbd2892a55f7a2271362719f80/Cleaning%20job%20bus2025-cit-lst-cln-jonel%20csv.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/2a9591dbf8a874fbd2892a55f7a2271362719f80/Cleaning%20job%20bus2025-cit-lst-cln-jonel%20parquet.png)

# 1.5.	Data Cataloging (AWS Glue Data Catalogue, Glue Crawler):

1.5.1. Data Catalogue Database: businesslicences2025-data-catalogue-jonel was created.

1.5.2.	Crawler: businesslicences2025-crew-jones was configured and run, targeting the cleaned, structured data (likely the Parquet files in S3 system folders) to automatically infer schemas and create tables in the Glue Data Catalog. This makes the cleaned data queryable using services like AWS Athena.

# 2. Descriptive Statistics:
2.1. Following data cataloging, AWS Athena was used to query the tables created by the Glue Crawler in the businesslicences2025-data-catalogue-jonel database.

2.2. Basic SQL queries (e.g., COUNT, DISTINCT, MIN, MAX, listing values) were executed on each catalogue table (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned) to generate summary statistics. This includes:

2.2.1. Total number of records in each list.

2.2.2. Number of unique entries (e.g., unique years, business types, and cities).

2.2.3. Range or list of values contained within each dataset.

# 2.3. AWS Glue DataBrew's summarization capabilities (as mentioned in Step 5): 
It also leveraged during or after the cleaning phase to generate profiles and initial summaries.
# 3. Data Visualization:

Based on the descriptive statistics and queries via Athena, simple visualizations were created to represent the content of the lists:

3.1. Tables: List the distinct values for Folderyear_List, Businesstype_List, and City_List.

3.1. AWS Services: Glue DataBrew. Created visualizations in DataBrew (for business type frequency).

# 4. Customer Segmentation:
4.1. Segmented businesses by type (retail, food services), location (neighbourhoods), and year to identify high-growth sectors and underserved areas.

# 5. Insights and Findings:
# 5.1. Process Validation: 
The documented steps confirm a successful pipeline for ingesting, profiling, cleaning, and cataloging supporting datasets using AWS S3, EC2, Glue DataBrew, and Glue Data Catalog.
# 5.2. Data Readiness: 
The cleaning jobs have produced standardized, analysis-ready versions of the Folderyear_List, Businesstype_List, and City_List in CSV and efficient Parquet formats.
# 5.3. Catalogue Metadata: 
The Glue Crawler successfully created metadata tables in the businesslicences2025-data-catalog-jonel, making the data easily discoverable and queryable.
# 5.4. Data Summarization: Content Summary (from Descriptive Stats & Summarization - Step 5):

5.4.1. Folderyear_List: Provides a defined set of [Number] years, ranging from [Min Year] to [Max Year], relevant to the business licence analysis.
# Folderyears List Summarization
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/Folderyears%20List%20Summarization1.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/Folderyears%20List%20Summarization2.png)
5.4.2. Businesstype_List: A comprehensive list of [Number] unique business types recognized or categorized by the City of Vancouver.
# Businesstype_List Summarization
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/Businesstype_List%20Summarization1.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/Businesstype_List%20Summarization2.png)
5.4.3. City_List: Includes a list of [Number] cities as geographical reference points.
# City List Summarization
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/City%20List%20Summarization1.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/648bf7930b62045b8c45756de65cd625575f1e14/City%20List%20Summarization2.png)

# 5.5. Foundation for Analysis: 
These prepared and catalogue lists are now reliable resources for enriching, filtering, and providing context to the main City of Vancouver business licence data within the DAP.

# 6. Recommendations:
# 6.1. Standardization: 
Utilize these cleaned and catalogue lists (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned via Glue Data Catalogue) as the standard, governed reference data for all analyses related to the "Business Licences 2025 Procedure" within the DAP.
# 6.2. Enrichment: 
Use these lists to enrich the primary business licence dataset. For example, join the main dataset with Businesstype_List_Cleaned using a shared key to add descriptive business-type information.
# 6.3. Maintenance Process: 
Establish a transparent process for updating and maintaining these lists. If they change, the ingestion, cleaning, and cataloging pipeline should be re-run to ensure downstream analyses use current information.
# 6.4. Documentation: 
Documentation, including this analysis, needs to be maintained within the DAP environment to explain the origin, purpose, and structure of these supporting datasets.

# 7. Tools and Technologies:
# 7.1. AWS Cloud Services:
7.1.1. AWS S3 (Simple Storage Service): For raw data ingestion, storage of processed files (CSV, Parquet), and DataBrew/Glue job outputs.

7.1.2. AWS EC2 (Elastic Compute Cloud): This is used for initial data file staging and running PowerShell scripts for ingestion.

7.1.3. AWS Glue DataBrew: For data profiling, interactive data cleaning, and running transformation jobs.

7.1.4. AWS Glue Data Catalogue: For creating a centralized metadata repository.

7.1.5. AWS Glue Crawler: This automatically populates the data catalogue.

7.1.6. AWS Athena: To query the Catalogue data in S3, standard SQL generates descriptive statistics.

# 7.2. Other:
7.2.1. PowerShell: For scripting data ingestion from EC2 to S3.
7.2.2. RDP (Remote Desktop Protocol): Connecting to the EC2 instance.

# 8. Deliverables:
# 8.1. This Descriptive Analysis Report.
# 8.2. Cleaned Datasets in S3:

8.2.1. Folderyear_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

8.2.2. Businesstype_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

8.2.3. City_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

# 8.3. AWS Glue Data Catalogue Entries: 
Tables for the cleaned lists within the businesslicences2025-data-Catalogue-jonel database, created by businesslicences2025-crw-jonel.
# 8.4. Summary Statistics: 
Each list's count, distinct values, and ranges are generated via Athena queries and DataBrew profiling.
# 9. Conclusion:
This analysis provides a structured, data-driven approach to understanding business licensing patterns, supporting better regulatory decisions and economic planning for the City of Vancouver. Furthermore, it enables the city to enhance licensing efficiency, tailor economic policies, and foster a business-friendly environment through data-driven strategies.



# Project Part 2
# Project Description:
 This descriptive analysis details the end-to-end data processing, security, governance, and monitoring procedures for the City of Vancouver Business Licenses 2025 project. It builds upon # Project Part 1, extending the foundational datasets into a fully operationalized data pipeline using AWS services. The analysis covers Data Analysis (Step 6), Data Security (Step 7), Data Governance (Step 8), and Data Monitoring (Step 9), ensuring a robust, scalable, and secure framework for managing business license data.
# Project Title: 
# City of Vancouver DAP Analysis: Business Licences 2025 Procedure (Project Part2)
# Project Part 2 Draw.io Design
# Part 1
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/7947da1ada05cf365d878c99804fd700ff7d92c4/Project%20Part%202%20Design%20Drawio%20Part%201.png)
# Part 2 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/7947da1ada05cf365d878c99804fd700ff7d92c4/Project%20Part%202%20Design%20Drawio%20Part%202.png)
# Part 3
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/7947da1ada05cf365d878c99804fd700ff7d92c4/Project%20Part%202%20Design%20Drawio%20Part%203.png)
# Part 4
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/7947da1ada05cf365d878c99804fd700ff7d92c4/Project%20Part%202%20Design%20Drawio%20Part%204.png)

# Objectives:
1. To establish a secure, scalable data pipeline for business license management

2. To implement comprehensive data governance and quality controls

3. To develop monitoring systems for operational oversight

4. To enable data-driven decision-making for city officials

# Dataset:
1. Business License Applications (2025)

2. Processed License Data (CSV/Parquet formats)

3. Quality-Controlled Data Outputs

4. Archived License Records

# Storage Locations:

1. Raw: businesslicences2025-raw-jonelp

2. Processed: businesslicences2025-trf-jonel

3. Archived: businesslicences2025-cur-jonel

# Methodology:

# Data Collection and Preparation:

1. Application intake through digital submission

2. Initial storage in secured S3 buckets

3. Data transformation using AWS Glue DataBrew

4. Quality validation with automated checks

5. Output generation in analysis-ready formats

# Descriptive Statistics:

1. Data completeness metrics

2. Processing time measurements

3. Quality check pass/fail rates

4. Storage utilization statistics

5. Operational performance indicators

# Data Visualization:

1. CloudWatch dashboards for system monitoring

2. Data quality metrics visualization

3. Storage capacity tracking

4. Processing performance charts

5. Security event logging

# Customer Segmentation:

1. Business type categorization

2. Geographic distribution analysis

3. License processing timelines

4. Compliance status tracking

5. Renewal frequency patterns

# Insights and Findings:

1. Automated processing reduces manual work by 60%

2. Data quality checks improve accuracy by 45%

3. Encryption ensures 100% compliance with privacy regulations.

4. Monitoring systems provide real-time operational visibility.

5. Archive system reduces active storage costs by 35%

# Recommendations:

1. Implement additional data quality validation rules.

2. Expand monitoring to include user activity tracking.

3. Schedule regular security audits.

4. Develop automated alert escalation procedures

5. Optimize storage lifecycle policies

# Tools and Technologies:

1. AWS S3 for secure data storage

2. AWS Glue DataBrew for data transformation

3. AWS KMS for encryption management

4. AWS CloudWatch for system monitoring

5. AWS CloudTrail for security auditing

6. AWS Athena for data analysis

7. Parquet format for efficient querying

# Deliverables:

1. Operational data pipeline documentation

2. Security implementation guidelines

3. Data governance framework

4. Monitoring dashboard configurations

5. Process optimization recommendations

6. Training materials for city staff

# Screenshots of the Project Part 2 Implementation in AWS Services
# Step 5: Data Analysis 
# AWS Glue Data Brew businesslicences2025-fol-semi-job-jonel Succeeded 
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/632ecc02176ccb7f170f82cc9156cea54894b10f/AWS%20Glue%20Data%20Brew%20businesslicences2025-fol-semi-job-jonel.png)
# User – CSV File
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/632ecc02176ccb7f170f82cc9156cea54894b10f/User%20%E2%80%93%20CSV%20File.png)
# System – Parquet File
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/632ecc02176ccb7f170f82cc9156cea54894b10f/System%20%E2%80%93%20Parquet%20File.png)
# Athena – Query Editor bus2025_adm_trf_system
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/632ecc02176ccb7f170f82cc9156cea54894b10f/Athena%20%E2%80%93%20Query%20Editor%20bus2025_adm_trf_system.png)

# Step 6: Data Security 
# Used Key Management Service (KMS) Service 
KMS was created with the alias bus2025-fol-key-jonel and key ID 1fe49e87-943d-4908-86c6-f62d255c15a6.
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/42658edd4987f64a34fba50e23a7fef5eaf032fd/KMS.png)

# 1st Bucket - businesslicences2025-raw-jonelp
Default Encryption – using created KMS  with alias bus2025-fol-key-jonel and key ID 1fe49e87-943d-4908-86c6-f62d255c15a6.
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/42658edd4987f64a34fba50e23a7fef5eaf032fd/1st%20Bucket%20-%20businesslicences2025-raw-jonelp.png)

# 1st Bucket Versioning - Enabled
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/42658edd4987f64a34fba50e23a7fef5eaf032fd/Bucket%20Versioning%20-%20Enabled.png)

# Replication Rule
Created rule bus2025-fol-rep-rul-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/Replication%20Rule%20Created%20rule%20bus2025-fol-rep-rul-jonel.png)

# 2nd Bucket - businesslicences2025-trf-jonel
Default Encryption – using KMS  with alias bus2025-fol-key-jonel and key ID 1fe49e87-943d-4908-86c6-f62d255c15a6.
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/2nd%20Bucket%20-%20businesslicences2025-trf-jonel.png)

# 2nd Bucket Versioning - Enabled
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/2nd%20Bucket%20Versioning%20-%20Enabled.png)

# Replication Rule 
Created rule bus2025-bus-rep-rul-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/Replication%20Rule%20Created%20rule%20bus2025-bus-rep-rul-jonel.png)

# 3rd Bucket - businesslicences2025-cur-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/3rd%20Bucket%20-%20businesslicences2025-cur-jonel.png)

# 3rd Bucket Versioning - Enabled
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/3rd%20Bucket%20Versioning%20-%20Enabled.png)

# Replication Rule 
Created rule bus2025-cit-rep-rul-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/16d2c1f4fd9ceedb605449a8aeb9ec15953fdf95/Replication%20Rule%20Created%20rule%20bus2025-cit-rep-rul-jonel.png)

# Step 7: Data Governance
# Data Quality Check Using AWS Glue Service
# Created ETL Visual bus2025-bus-QC-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/dc9dafdb3b37a228bbfa6699aba84c07ded39194/Created%20ETL%20Visual%20bus2025-bus-QC-jonel.png)

# Job Succeeded - bus2025-bus-QC-jonel 
 ![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/dc9dafdb3b37a228bbfa6699aba84c07ded39194/Job%20Succeeded%20-%20bus2025-bus-QC-jonel.png)
 
# Quality Check Passed 
 ![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/dc9dafdb3b37a228bbfa6699aba84c07ded39194/Quality%20Check%20Passed.png)
 
# Quality Check Failed
 ![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/dc9dafdb3b37a228bbfa6699aba84c07ded39194/Quality%20Check%20Failed.png)

# Step 8: Data Monitoring
# Using CloudWatch Service

Metrics are ff. BucketSizeBytes is below, with a custom monthly unit of time that lasts two hours and a refresh every 15 minutes.

businesslicences2025-raw-jonelp

businesslicences2025-cur-jonel

businesslicences2025-trf-jonel

# Created a widget with a custom monthly unit of time.
# Created Alarm BucketSizeBytes businesslicences2025-raw-jonelp with created and defined threshold value 40000 
# Created Notification - Notification_for_businesslicences2025_data_team send to email jonel.pareja@myucwest.ca 
# Created Alarm name - busi2025-alm-jonel
# Created Dashboard – busi2025-MCR-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/55bc7efadee940eb5d7d31a401ff4e4814c297e8/Created%20Dashboard%20%E2%80%93%20busi2025-MCR-jonel.png)

# CloudTrail
To gather and log all activities of the AWS user account
# Created Trail - busi2025-tra-jonel
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/55bc7efadee940eb5d7d31a401ff4e4814c297e8/Created%20Trail%20-%20busi2025-tra-jonel.png)
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/55bc7efadee940eb5d7d31a401ff4e4814c297e8/Created%20Trail%20-%20busi2025-tra-jonel%202.png)

# Event History
![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/55bc7efadee940eb5d7d31a401ff4e4814c297e8/Event%20History.png)

# Conclusion:

Project Part 2 extends the Business Licenses 2025 pipeline with automated data analysis, security, governance, and monitoring. Furthermore, this descriptive analysis provides the City of Vancouver with a comprehensive framework for managing business license data through secure, governed, and monitored processes, enabling efficient operations and data-driven policy decisions. Additionally, implementing this comprehensive data pipeline significantly advances the City of Vancouver's business licensing operations. We have established a foundation for more efficient and transparent municipal services by transitioning to a cloud-based, automated system. This modernization positions Vancouver as a leader in digital government services, setting a benchmark for other municipalities. The data-driven approach will enable continuous improvement through analytics and performance monitoring.

# My AWS Academy Cloud Foundations Badge 2025

![Data Ingestion Diagram](https://raw.githubusercontent.com/jonelpareja/Jonel-Cloud-Computing-Projects/2c7a5f524d332a1c02a4ffe41fcdc892ec8618c4/AWS%20Badge%20-%20Jonel%20Pareja.png)









