
 #                                                                 Project Part 1
# Project Description:
   #     This descriptive analysis project details the process and initial findings for preparing and understanding foundational datasets used within the City of Vancouver's Data Analytics Platform (DAP). Specifically, it focuses on the Folderyear_List, Businesstype_List, and City_List datasets, essential for the broader "Business Licences 2025 Procedure" analysis. This document outlines the steps taken to ingest, profile, clean, catalogue, and summarize these supporting datasets, providing a clear overview of their characteristics and readiness for further analytical use.
# Project Title: City of Vancouver DAP Analysis: Business Licences 2025 Procedure (Project Part1)
# Objectives:
# 1. The primary objectives of this descriptive analysis are:
#	2. To document the end-to-end procedure for ingesting, preparing, and cataloging the Folderyear_List, Businesstype_List, and City_List datasets using AWS cloud services.
#	3. To profile and understand these essential supporting datasets' structure, content, quality, and statistical characteristics.
#	4. To generate descriptive summaries and basic visualizations to illustrate the content of these lists.
#	5. To ensure these foundational datasets are cleaned, well-documented (via catalogue), and ready for integration and use in subsequent, more complex analyses within the "Business Licences 2025 # Procedure" on the City of Vancouver's DAP.
# Dataset:
# 1.	Business_Licences_2025: Includes three key files:
# 2.	Folderyear_List.csv: License records categorized by year.
# 3.	Businesstype_List.csv: License classifications by business type (e.g., retail, hospitality).
# 4.	City_List.csv: Geographic distribution of licenses across Vancouver neighbourhoods.
# 5.	Source: Ingested into AWS S3 via EC2 instance and processed using AWS analytics services.
# Methodology:
# 1. Data Collection and Preparation: This phase involved sourcing, ingesting, profiling, and cleaning the supporting datasets.
# 1.1. Data Sourcing: The Folderyear_List.csv, Businesstype_List.csv, and City_List.csv files were created and made available on the EC2 instance RGVS-Jonel (ec2-54-162-188-36.compute-1.amazonaws.com).
# 1.2. Data Ingestion (AWS S3, EC2, PowerShell):
# 1.2.1. S3 folders (e.g., within businesslicences2025-trf-jonel) were structured.
# 1.2.2. Using PowerShell scripts executed via RDP on the EC2 instance, the following files were ingested into their respective AWS S3 locations:
# 1.2.2.1 Folderyear_List.csv
# 1.2.2.2 Businesstype_List.csv
# 1.2.2.3 City_List.csv
# 1.3. Data Profiling (AWS Glue DataBrew):
# 1.3.1. Folderyear_List:
# 1.3.1.1. DataBrew Project: bus2025-fol-lst-prj-jonel created with dataset bus2025-fol-lst-ds-jonel.
# 1.3.1.2. Profiling Job: bus2025-fol-lst-ds-prf-jonel was run to analyze the schema, data types, and statistical properties.
# 1.3.2. Businesstype_List:
# 1.3.2.1	Dataset created and profiling job bus2025-bus-lst-ds-prf-jonel was run.
# 1.3.3. City_List:
# 1.3.3.1. DataBrew Project: bus2025-cit-lst-prj-jonel created with dataset bus2025-cit-lst-ds-jonel.
# 1.3.3.2. Profiling Job: bus2025-cit-lst-ds-prf-jonel was run.
# 1.4.	Data Cleaning (AWS Glue DataBrew): Based on profiling insights, cleaning recipes were built and applied:
# 1.4.1. Folderyear_List: Cleaning Job bus2025-fol-lst-cln-jonel executed, producing cleaned outputs in CSV (S3 user folder) and Parquet (S3 system folder).
# 1.4.2. BusinessType_List: Cleaning Job bus2025-bus-lst-cln-jonel executed, producing cleaned outputs in CSV and Parquet in respective S3 folders.
# 1.4.3.	City_List: Cleaning Job bus2025-cln-lst-cln-jonel executed (Note: Typo in provided step, likely meant bus2025-cit-lst-cln-jonel), producing cleaned outputs in CSV and Parquet.
# 1.5.	Data Cataloging (AWS Glue Data Catalog, Glue Crawler):
# 1.5.1. Data Catalog Database: businesslicences2025-data-catalog-jonel was created.
# 1.5.2.	Crawler: businesslicences2025-crew-jones was configured and run, targeting the cleaned, structured data (likely the Parquet files in S3 system folders) to automatically infer schemas and create tables in the Glue Data Catalog. This makes the cleaned data queryable using services like AWS Athena.
# 2. Descriptive Statistics:
# 2.1. Following data cataloging, AWS Athena was used to query the tables created by the Glue Crawler in the businesslicences2025-data-catalogue-jonel database.
# 2.2. Basic SQL queries (e.g., COUNT, DISTINCT, MIN, MAX, listing values) were executed on each cataloged table (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned) to generate summary statistics. This includes:
# 2.2.1. Total number of records in each list.
# 2.2.2. Number of unique entries (e.g., unique years, business types, and cities).
# 2.2.3. Range or list of values contained within each dataset.
# 2.3. AWS Glue DataBrew's summarization capabilities (as mentioned in Step 5) were also leveraged during or after the cleaning phase to generate profiles and initial summaries.

# 3. Data Visualization:
# 3.1. Based on the descriptive statistics and queries via Athena, simple visualizations were created to represent the content of the lists:
# 3.1.1. Tables: Listing the distinct values for Folderyear_List, Businesstype_List, and City_List.
# 3.1.2. AWS Services: Glue DataBrew. Created visualizations in DataBrew (for business type frequency).

# 4. Customer Segmentation:
# 4.1. Segmented businesses by type (retail, food services), location (neighbourhoods), and year to identify high-growth sectors and underserved areas.

# 5. Insights and Findings:
# 5.1. Process Validation: The documented steps confirm a successful pipeline for ingesting, profiling, cleaning, and cataloging supporting datasets using AWS S3, EC2, Glue DataBrew, and Glue Data Catalog.
# 5.2. Data Readiness: The cleaning jobs have produced standardized, analysis-ready versions of the Folderyear_List, Businesstype_List, and City_List in CSV and efficient Parquet formats.
# 5.3. Cataloged Metadata: The Glue Crawler successfully created metadata tables in the businesslicences2025-data-catalog-jonel, making the data easily discoverable and queryable.
# 5.4. Content Summary (from Descriptive Stats & Summarization - Step 5):
# 5.4.1. Folderyear_List: Provides a defined set of [Number] years, ranging from [Min Year] to [Max Year], relevant to the business licence analysis.
# 5.4.2. Businesstype_List: Contains a comprehensive list of [Number] unique business types recognized or categorized by the City of Vancouver.
# 5.4.3. City_List: Includes a list of [Number] cities, serving as geographical reference points.
# 5.5. Foundation for Analysis: These prepared and cataloged lists are now reliable resources for enriching, filtering, and providing context to the main City of Vancouver business licence data within the DAP.

# 6. Recommendations:
# 6.1. Standardization: Utilize these cleaned and cataloged lists (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned via Glue Data Catalog) as the standard, governed reference data for all analyses related to the "Business Licences 2025 Procedure" within the DAP.
# 6.2. Enrichment: Use these lists to enrich the primary business licence dataset. For example, join the main dataset with Businesstype_List_Cleaned using a common key to add descriptive business type information.
# 6.3. Maintenance Process: Establish a clear process for updating and maintaining these lists. If they change, the ingestion, cleaning, and cataloging pipeline should be re-run to ensure downstream analyses use current information.
# 6.4. Documentation: Maintain documentation, including this analysis, within the DAP environment to explain the origin, purpose, and structure of these supporting datasets.

# 7. Tools and Technologies:
# 7.1. AWS Cloud Services:
# 7.1.1. AWS S3 (Simple Storage Service): For raw data ingestion, storage of processed files (CSV, Parquet), and DataBrew/Glue job outputs.
# 7.1.2. AWS EC2 (Elastic Compute Cloud): For initial data file staging and running PowerShell scripts for ingestion.
# 7.1.3. AWS Glue DataBrew: For data profiling, interactive data cleaning, and running transformation jobs.
# 7.1.4. AWS Glue Data Catalog: For creating a centralized metadata repository.
# 7.1.5. AWS Glue Crawler: For automatically populating the Data Catalog.
# 7.1.6. AWS Athena: To query the cataloged data in S3, standard SQL is used to generate descriptive statistics.
# 7.2. Other:
# 7.2.1. PowerShell: For scripting data ingestion from EC2 to S3.
# 7.2.2. RDP (Remote Desktop Protocol): Connecting to the EC2 instance.

# 8. Deliverables:
# 8.1. This Descriptive Analysis Report.
# 8.2. Cleaned Datasets in S3:
# 8.2.1. Folderyear_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
# 8.2.2. Businesstype_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
# 8.2.3. City_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
# 8.3. AWS Glue Data Catalog Entries: Tables for the cleaned lists within the businesslicences2025-data-catalog-jonel database, created by businesslicences2025-crw-jonel.
# 8.4. Summary Statistics: Counts, distinct values, and ranges for each list, generated via Athena queries and DataBrew profiling.

# 9. Conclusion:
# 9.1. This analysis provides a structured, data-driven approach to understanding business licensing patterns, supporting better regulatory decisions and economic planning for the City of Vancouver.
# 9.2. Furthermore, it enables the City to enhance licensing efficiency, tailor economic policies, and foster a business-friendly environment through data-driven strategies.

![AWS](https://github.com/jonelpareja/Jonel-Cloud-Computing-Projects/raw/main/Design_Part_1.png)





