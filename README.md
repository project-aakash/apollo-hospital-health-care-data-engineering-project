## Apollo Health Care Data Pipeline using Azure Data Factory
Introduction
The Apollo Health Care project aims to build a centralized data repository that serves as a single source of truth for Data Analytics and Data Science teams. This centralized table adheres to the Medallion Architecture (Bronze, Silver, and Gold layers), ensuring scalability, data integrity, and optimized performance.

Business Requirement Document (BRD)
Project Objective
The objective of this project is to build a centralized data repository that serves as a single source of truth for Data Analytics and Data Science teams.

Key Considerations
Medallion Architecture Implementation

Bronze Layer: Raw, unprocessed data ingestion.

Silver Layer: Standardized, cleaned, and enriched data with schema validation.

Gold Layer: Aggregated, business-ready data optimized for analytics and AI models.

Data Dictionary
Provider
This table contains 50 provider information.

Prov_id: Provider ID

Prov_name: Provider Name

Prov_loc_id: Providers location id

Prov_specialty: Provider’s Specialty

Locations
This table contains location information for patients’ visit and providers’ location.

Loc_id: Location ID

Loc_name: Location Name

Sa_name: Service Area Name

Patient
This table contains patient information.

Unique_Patient_id: Patient unique ID

Gender_c: Patient’s Gender (“M”,”F”)

Birth_date: Patients’ Birthdate

Pat_loc_id: The patient’s primary location

Pcp
This table contains patient’s primary care provider information.

Unique_Patient_id: Patient ID

Pcp_prov_id: Primary care provider id

Encounters
This table contains encounter information.

Enc_id: Encounter ID for every encounter visit

Enc_Patient_id: Patient ID associated with the encounter

Visit_prov_id: Provider id for encounter

Enc_Status_c: Status of the encounter (“Completed”, “Cancelled”)

Enc_date: Date associated with the visit

Due_Date: Recorded due date for pregnant patients

Encounter_dx
The table contains diagnosis information related to the encounter.

Enc_id: Unique Encounter ID

Line: The line number for the diagnosis associated with this record. Multiple pieces of diagnosis can be associated with this record.

Icd_code: ICD 10 diagnosis code regarding to the diagnosis

Pregnancy_Diagnosis
This table contains diagnosis information for identifying pregnancy diagnosis.

Code: Diagnosis code for pregnancy diagnosis

Implementation Steps
Step 1: Data Ingestion
Bronze Layer: Raw data ingestion from multiple sources such as CSV files, databases, and APIs into the Bronze layer.

Step 2: Data Cleaning and Transformation
Silver Layer: Standardizing, cleaning, and enriching the raw data. Applying schema validation to ensure data integrity.

Step 3: Data Aggregation and Optimization
Gold Layer: Aggregating the cleaned data to create business-ready datasets optimized for analytics and AI models.

Step 4: Data Storage and Access
Storing the data in Azure Data Lake and providing access to the Data Analytics and Data Science teams.

Results and Analysis
Scalability: The centralized data repository can scale easily to accommodate growing data volumes.

Data Integrity: Schema validation ensures the accuracy and consistency of the data.

Performance: Optimized data layers improve query performance for analytics and AI models.

Conclusion
The Apollo Health Care Data Pipeline using Azure Data Factory successfully builds a centralized data repository that adheres to the Medallion Architecture. This implementation ensures scalability, data integrity, and optimized performance, making it a valuable resource for Data Analytics and Data Science teams.
