# Project Part 1
# Project Description:
 This descriptive analysis project details the process and initial findings for preparing and understanding foundational datasets used within the City of Vancouver's Data Analytics Platform (DAP). Specifically, it focuses on the Folderyear_List, Businesstype_List, and City_List datasets, essential for the broader "Business Licences 2025 Procedure" analysis. This document outlines the steps taken to ingest, profile, clean, catalogue, and summarize these supporting datasets, providing a clear overview of their characteristics and readiness for further analytical use.
# Project Title: 
City of Vancouver DAP Analysis: Business Licences 2025 Procedure (Project Part1)
# Project Part 1 Draw.io Design
# Part 1
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%201.png)
# Part 2 
![AAWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%202.png)
# Part 3
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%203.png)
# Part 4
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/8da8a429f4c9156813b1ae2a2ae9d5a150cd7572/Design%20Part%204.png)

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
# Screenshots of the Project Implementation in AWS Services
# Created 3 folders in AWS S3
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/4309f958d38e2dac624bb5697e141820b8edf692/Created%203%20folders%20in%20AWS%20S3.png)
# Created EC2 Instance RGVS-Jonel
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/Created%20EC2%20Instance%20RGVS-Jonel.png)
# Connected to EC2 via RDP and created list of csv files 
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/s3%20folder%20created.png)
# Connected to EC2 via RDP and created 3 CSV files) 
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/folders%20list%20and%20connected%20to%20rdp.png)
# Data Ingestion using Powershell Script (EC2 RDP) to S3
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/Data%20Ingestion%20using%20Powershell%20%20(EC2%20RDP)%20to%20S3.png)
# Folderyear_List.csv S3 location
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/Folderyear_List.csv%20S3%20location%20.png)
# Businesstype_List.csv in S3 location
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/Businesstype_List.csv%20%20S3%20location.png)
# City_List CSV in S3 location
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/98d9638de72f17d1bbdb782414b247b926adec5e/City_List%20CSV%20S3%20location.png)


# 1.3. Data Profiling (AWS Glue DataBrew):
# 1.3.1. Folderyear_List:

1.3.1.1. DataBrew Project: bus2025-fol-lst-prj-jonel created with dataset bus2025-fol-lst-ds-jonel

1.3.1.2. Profiling Job: bus2025-fol-lst-ds-prf-jonel was run to analyze the schema, data types, and statistical properties

# Folderyear_List: Created project name  bus2025-fol-lst-prj-jonel project and dataset name bus2025-fol-lst-ds-jonel
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/bdc4ebe758e557f65708ded3fe31d501e2ce38a0/Folderyear_List%20data%20profiling1.png)
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/bdc4ebe758e557f65708ded3fe31d501e2ce38a0/Folderyear_List%20data%20profiling2.png)
# Created and run the job bus2025-fol-lst-ds-prf-jonel
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/afb8f2e855228131ef52d10fb5adcbc589b9403c/Created%20and%20run%20the%20job%20bus2025-fol-lst-ds-prf-jonel.png)

# 1.3.2. Businesstype_List:

1.3.2.1	Dataset created and profiling job bus2025-bus-lst-ds-prf-jonel was run.

# 1.3.3. City_List:

1.3.3.1. DataBrew Project: bus2025-cit-lst-prj-jonel created with dataset bus2025-cit-lst-ds-jonel.

1.3.3.2. Profiling Job: bus2025-cit-lst-ds-prf-jonel was run.

# 1.4.	Data Cleaning (AWS Glue DataBrew): 
Based on profiling insights, cleaning recipes were built and applied:

1.4.1. Folderyear_List: Cleaning Job bus2025-fol-lst-cln-jonel executed, producing cleaned outputs in CSV (S3 user folder) and Parquet (S3 system folder).

# Cleaning job bus2025-fol-lst-cln-jonel  csv and parquet stored in S3 User and System folders, respectively.

![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/f9f59f2f3514f4785407e22afb1ef5671756ce15/data%20cleaning%202.png)

![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/f9f59f2f3514f4785407e22afb1ef5671756ce15/data%20cleaning3.png)

1.4.2. BusinessType_List: Cleaning Job bus2025-bus-lst-cln-jonel executed, producing cleaned outputs in CSV and Parquet in respective S3 folders.

1.4.3.	City_List: Cleaning Job bus2025-cln-lst-cln-jonel executed (Note: Typo in provided step, likely meant bus2025-cit-lst-cln-jonel), producing cleaned outputs in CSV and Parquet.




# 1.5.	Data Cataloging (AWS Glue Data Catalog, Glue Crawler):

1.5.1. Data Catalog Database: businesslicences2025-data-catalog-jonel was created.

1.5.2.	Crawler: businesslicences2025-crew-jones was configured and run, targeting the cleaned, structured data (likely the Parquet files in S3 system folders) to automatically infer schemas and create tables in the Glue Data Catalog. This makes the cleaned data queryable using services like AWS Athena.


# 2. Descriptive Statistics:
2.1. Following data cataloging, AWS Athena was used to query the tables created by the Glue Crawler in the businesslicences2025-data-catalogue-jonel database.

2.2. Basic SQL queries (e.g., COUNT, DISTINCT, MIN, MAX, listing values) were executed on each cataloged table (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned) to generate summary statistics. This includes:

2.2.1. Total number of records in each list.

2.2.2. Number of unique entries (e.g., unique years, business types, and cities).

2.2.3. Range or list of values contained within each dataset.

# 2.3. AWS Glue DataBrew's summarization capabilities (as mentioned in Step 5): 
It also leveraged during or after the cleaning phase to generate profiles and initial summaries.
# 3. Data Visualization:

Based on the descriptive statistics and queries via Athena, simple visualizations were created to represent the content of the lists:

3.1. Tables: Listing the distinct values for Folderyear_List, Businesstype_List, and City_List.

3.1. AWS Services: Glue DataBrew. Created visualizations in DataBrew (for business type frequency).

# 4. Customer Segmentation:
4.1. Segmented businesses by type (retail, food services), location (neighbourhoods), and year to identify high-growth sectors and underserved areas.

# 5. Insights and Findings:
# 5.1. Process Validation: 
The documented steps confirm a successful pipeline for ingesting, profiling, cleaning, and cataloging supporting datasets using AWS S3, EC2, Glue DataBrew, and Glue Data Catalog.
# 5.2. Data Readiness: 
The cleaning jobs have produced standardized, analysis-ready versions of the Folderyear_List, Businesstype_List, and City_List in CSV and efficient Parquet formats.
# 5.3. Cataloged Metadata: 
The Glue Crawler successfully created metadata tables in the businesslicences2025-data-catalog-jonel, making the data easily discoverable and queryable.
# 5.4. Data Summarization: Content Summary (from Descriptive Stats & Summarization - Step 5):

5.4.1. Folderyear_List: Provides a defined set of [Number] years, ranging from [Min Year] to [Max Year], relevant to the business licence analysis.
# Folderyears List Summarization
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/Folderyears%20List%20Summarization1.png)
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/Folderyears%20List%20Summarization2.png)
5.4.2. Businesstype_List: A comprehensive list of [Number] unique business types recognized or categorized by the City of Vancouver.
# Businesstype_List Summarization
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/Businesstype_List%20Summarization1.png)
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/Businesstype_List%20Summarization2.png)
5.4.3. City_List: Includes a list of [Number] cities as geographical reference points.
# City List Summarization
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/City%20List%20Summarization1.png)
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/648bf7930b62045b8c45756de65cd625575f1e14/City%20List%20Summarization2.png)

# 5.5. Foundation for Analysis: 
These prepared and cataloged lists are now reliable resources for enriching, filtering, and providing context to the main City of Vancouver business licence data within the DAP.

# 6. Recommendations:
# 6.1. Standardization: 
Utilize these cleaned and cataloged lists (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned via Glue Data Catalog) as the standard, governed reference data for all analyses related to the "Business Licences 2025 Procedure" within the DAP.
# 6.2. Enrichment: 
Use these lists to enrich the primary business licence dataset. For example, join the main dataset with Businesstype_List_Cleaned using a common key to add descriptive business type information.
# 6.3. Maintenance Process: 
Establish a clear process for updating and maintaining these lists. If they change, the ingestion, cleaning, and cataloging pipeline should be re-run to ensure downstream analyses use current information.
# 6.4. Documentation: 
Maintain documentation, including this analysis, within the DAP environment to explain these supporting datasets' origin, purpose, and structure.

# 7. Tools and Technologies:
# 7.1. AWS Cloud Services:
7.1.1. AWS S3 (Simple Storage Service): For raw data ingestion, storage of processed files (CSV, Parquet), and DataBrew/Glue job outputs.

7.1.2. AWS EC2 (Elastic Compute Cloud): For initial data file staging and running PowerShell scripts for ingestion.

7.1.3. AWS Glue DataBrew: For data profiling, interactive data cleaning, and running transformation jobs.

7.1.4. AWS Glue Data Catalog: For creating a centralized metadata repository.

7.1.5. AWS Glue Crawler: This is used to automatically populate the data catalog.

7.1.6. AWS Athena: To query the cataloged data in S3, standard SQL is used to generate descriptive statistics.

# 7.2. Other:
7.2.1. PowerShell: For scripting data ingestion from EC2 to S3.
7.2.2. RDP (Remote Desktop Protocol): Connecting to the EC2 instance.

# 8. Deliverables:
# 8.1. This Descriptive Analysis Report.
# 8.2. Cleaned Datasets in S3:

8.2.1. Folderyear_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

8.2.2. Businesstype_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

8.2.3. City_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.

# 8.3. AWS Glue Data Catalog Entries: 
Tables for the cleaned lists within the businesslicences2025-data-catalog-jonel database, created by businesslicences2025-crw-jonel.
# 8.4. Summary Statistics: 
Each list's count, distinct values, and ranges are generated via Athena queries and DataBrew profiling.

# 9. Conclusion:
This analysis provides a structured, data-driven approach to understanding business licensing patterns, supporting better regulatory decisions and economic planning for the City of Vancouver. Furthermore, it enables the city to enhance licensing efficiency, tailor economic policies, and foster a business-friendly environment through data-driven strategies.


# Project Part 2
# Project Description:
 This descriptive analysis project details the process and initial findings for preparing and understanding foundational datasets used within the City of Vancouver's Data Analytics Platform (DAP). Specifically, it focuses on the Folderyear_List, Businesstype_List, and City_List datasets, essential for the broader "Business Licences 2025 Procedure" analysis. This document outlines the steps taken to ingest, profile, clean, catalogue, and summarize these supporting datasets, providing a clear overview of their characteristics and readiness for further analytical use.
# Project Title: 
City of Vancouver DAP Analysis: Business Licences 2025 Procedure (Project Part2)
# Project Part 2 Draw.io Design
# Part 1
![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/blob/7947da1ada05cf365d878c99804fd700ff7d92c4/Project%20Part%202%20Design%20Drawio%20Part%201.png)
# Part 2 
![AAWS]()
# Part 3
![AWS]()
# Part 4
![AWS]()








