# cloudcomputingprojects
BUSI653 Section 5 Cloud Computing Projects
                                                                  Project Part 1
Project Description:
        This descriptive analysis project details the process and initial findings related to preparing and understanding foundational datasets used within the City of Vancouver's Data Analytics Platform (DAP). Specifically, it focuses on the Folderyear_List, Businesstype_List, and City_List datasets, essential for the broader "Business Licences 2025 Procedure" analysis. This document outlines the steps taken to ingest, profile, clean, catalogue, and summarize these supporting datasets, providing a clear overview of their characteristics and readiness for further analytical use.
Project Title: City of Vancouver DAP Analysis: Business Licences 2025 Procedure
Objectives:
        The primary objectives of this descriptive analysis are:
•	To document the end-to-end procedure for ingesting, preparing, and cataloging the Folderyear_List, Businesstype_List, and City_List datasets using AWS cloud services.
•	To profile and understand these essential supporting datasets' structure, content, quality, and statistical characteristics.
•	To generate descriptive summaries and basic visualizations to illustrate the content of these lists.
•	To ensure these foundational datasets are cleaned, well-documented (via catalogue), and ready for integration and use in subsequent, more complex analyses within the "Business Licences 2025 Procedure" on the City of Vancouver's DAP.
Dataset:
•	Business_Licences_2025: Includes three key files:
•	Folderyear_List.csv: License records categorized by year.
•	Businesstype_List.csv: License classifications by business type (e.g., retail, hospitality).
•	City_List.csv: Geographic distribution of licenses across Vancouver neighbourhoods.
•	Source: Ingested into AWS S3 via EC2 instance and processed using AWS analytics services.
Methodology:
        1. Data Collection and Preparation: This phase involved sourcing, ingesting, profiling, and cleaning the supporting datasets.
•	Data Sourcing: The Folderyear_List.csv, Businesstype_List.csv, and City_List.csv files were created and made available on the EC2 instance RGVS-Jonel (ec2-54-162-188-36.compute-1.amazonaws.com).
•	Data Ingestion (AWS S3, EC2, PowerShell):
•	S3 folders (e.g., within businesslicences2025-trf-jonel) were structured.
•	Using PowerShell scripts executed via RDP on the EC2 instance, the following files were ingested into their respective AWS S3 locations:
•	Folderyear_List.csv
•	Businesstype_List.csv
•	City_List.csv
•	Data Profiling (AWS Glue DataBrew):
•	Folderyear_List:
•	DataBrew Project: bus2025-fol-lst-prj-jonel created with dataset bus2025-fol-lst-ds-jonel.
•	Profiling Job: bus2025-fol-lst-ds-prf-jonel was run to analyze the schema, data types, and statistical properties.
•	Businesstype_List:
•	Dataset created and profiling job bus2025-bus-lst-ds-prf-jonel was run.
•	City_List:
•	DataBrew Project: bus2025-cit-lst-prj-jonel created with dataset bus2025-cit-lst-ds-jonel.
•	Profiling Job: bus2025-cit-lst-ds-prf-jonel was run.
•	Data Cleaning (AWS Glue DataBrew): Based on profiling insights, cleaning recipes were built and applied:
•	Folderyear_List: Cleaning Job bus2025-fol-lst-cln-jonel executed, producing cleaned outputs in CSV (S3 user folder) and Parquet (S3 system folder).
•	BusinessType_List: Cleaning Job bus2025-bus-lst-cln-jonel executed, producing cleaned outputs in CSV and Parquet in respective S3 folders.
•	City_List: Cleaning Job bus2025-cln-lst-cln-jonel executed (Note: Typo in provided step, likely meant bus2025-cit-lst-cln-jonel), producing cleaned outputs in CSV and Parquet.
•	Data Cataloging (AWS Glue Data Catalog, Glue Crawler):
•	Data Catalog Database: businesslicences2025-data-catalog-jonel was created.
•	Crawler: businesslicences2025-crew-jones was configured and run, targeting the cleaned, structured data (likely the Parquet files in S3 system folders) to automatically infer schemas and create tables in the Glue Data Catalog. This makes the cleaned data queryable using services like AWS Athena.
2.	Descriptive Statistics:
•	Following data cataloging, AWS Athena was used to query the tables created by the Glue Crawler in the businesslicences2025-data-catalogue-jonel database.
•	Basic SQL queries (e.g., COUNT, DISTINCT, MIN, MAX, listing values) were executed on each cataloged table (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned) to generate summary statistics. This includes:
•	Total number of records in each list.
•	Number of unique entries (e.g., unique years, business types, and cities).
•	Range or list of values contained within each dataset.
•	AWS Glue DataBrew's summarization capabilities (as mentioned in Step 5) were also leveraged during or after the cleaning phase to generate profiles and initial summaries.
3.	Data Visualization:
Based on the descriptive statistics and queries via Athena, simple visualizations were created to represent the content of the lists:
•	Tables: Listing the distinct values for Folderyear_List, Businesstype_List, and City_List.
•	AWS Services: Glue DataBrew. Created visualizations in DataBrew (for business type frequency).
4.	Customer Segmentation:
•	Segmented businesses by type (retail, food services), location (neighbourhoods), and year to identify high-growth sectors and underserved areas.
5.	Insights and Findings:
•	Process Validation: The documented steps confirm a successful pipeline for ingesting, profiling, cleaning, and cataloging supporting datasets using AWS S3, EC2, Glue DataBrew, and Glue Data Catalog.
•	Data Readiness: The cleaning jobs have produced standardized, analysis-ready versions of the Folderyear_List, Businesstype_List, and City_List in CSV and efficient Parquet formats.
•	Cataloged Metadata: The Glue Crawler successfully created metadata tables in the businesslicences2025-data-catalog-jonel, making the data easily discoverable and queryable.
•	Content Summary (from Descriptive Stats & Summarization - Step 5):
•	Folderyear_List: Provides a defined set of [Number] years, ranging from [Min Year] to [Max Year], relevant to the business licence analysis.
•	Businesstype_List: Contains a comprehensive list of [Number] unique business types recognized or categorized by the City of Vancouver.
•	City_List: Includes a list of [Number] cities, serving as geographical reference points.
•	Foundation for Analysis: These prepared and cataloged lists are now reliable resources for enriching, filtering, and providing context to the main City of Vancouver business licence data within the DAP.
6.	Recommendations:
•	Standardization: Utilize these cleaned and cataloged lists (Folderyear_List_Cleaned, Businesstype_List_Cleaned, City_List_Cleaned via Glue Data Catalog) as the standard, governed reference data for all analyses related to the "Business Licences 2025 Procedure" within the DAP.
•	Enrichment: Use these lists to enrich the primary business licence dataset. For example, join the main dataset with Businesstype_List_Cleaned using a common key to add descriptive business type information.
•	Maintenance Process: Establish a clear process for updating and maintaining these lists. If they change, the ingestion, cleaning, and cataloging pipeline should be re-run to ensure downstream analyses use current information.
•	Documentation: Maintain documentation, including this analysis, within the DAP environment to explain the origin, purpose, and structure of these supporting datasets.

Tools and Technologies:
•	AWS Cloud Services:
•	AWS S3 (Simple Storage Service): For raw data ingestion, storage of processed files (CSV, Parquet), and DataBrew/Glue job outputs.
•	AWS EC2 (Elastic Compute Cloud): For initial data file staging and running PowerShell scripts for ingestion.
•	AWS Glue DataBrew: For data profiling, interactive data cleaning, and running transformation jobs.
•	AWS Glue Data Catalog: For creating a centralized metadata repository.
•	AWS Glue Crawler: For automatically populating the Data Catalog.
•	AWS Athena: To query the cataloged data in S3, standard SQL is used to generate descriptive statistics.
•	Other:
•	PowerShell: For scripting data ingestion from EC2 to S3.
•	RDP (Remote Desktop Protocol): Connecting to the EC2 instance.

Deliverables:
•	This Descriptive Analysis Report.
•	Cleaned Datasets in S3:
•	Folderyear_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
•	Businesstype_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
•	City_List: Cleaned CSV and Parquet files in businesslicences2025-trf-jonel S3 bucket.
•	AWS Glue Data Catalog Entries: Tables for the cleaned lists within the businesslicences2025-data-catalog-jonel database, created by businesslicences2025-crw-jonel.
•	Summary Statistics: Counts, distinct values, and ranges for each list, generated via Athena queries and DataBrew profiling.


        This analysis provides a structured, data-driven approach to understanding business
licensing patterns, supporting better regulatory decisions and economic planning for the City of Vancouver. Furthermore, it enables the City to enhance licensing efficiency, tailor economic policies, and foster a business-friendly environment through data-driven strategies.

