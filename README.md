# Property Investment Portfolio Project: Bus-Matrix-and-Data-Modeling

Before initiating the data modeling process, I developed a data pipeline using SSIS to ingest and stage data into six staging tables:

Stag_Aus_Suburb, Stag_Aus_Crime, Stag_HouseValue, Stag_RentalValue, Stag_Transport, and Stag_School.

This staging layer ensured clean, structured, and consistent data ready for transformation and modeling.

<a href="https://github.com/utkarshdatawhiz993/Bus-Matrix-and-Data-Modeling/blob/main/Six%20Staging%20Tables%20(ETL).pdf">Click for details of staging tables</a>

After organizing and preparing the staging tables, I developed a Bus Matrix to define the core business processes and shared dimensions. This step was essential in designing a scalable and consistent data model structure, ensuring alignment across different subject areas before proceeding with the modeling phase.

<a href="https://github.com/utkarshdatawhiz993/Bus-Matrix-and-Data-Modeling/blob/main/Screenshot%202025-07-31%20at%2011.39.01%20AM.png">Click here for bus matrix design</a>

Based on the datasets and the Bus Matrix, I implemented a hybrid data model combining both star and snowflake schema designs to optimize performance and maintain scalability. The model includes three fact tables:

Fact_HouseValue

Fact_RentalAmount

Fact_Incidents

Alongside, I designed five dimension tables:

Dim_Transport

Dim_School

Dim_Location

Dim_Crime

Dim_Rental

In this structure, Dim_Transport and Dim_School are normalized and connected to Dim_Location through a one-level join, creating a snowflake pattern. Dim_Location then connects directly to all three fact tables, serving as a shared dimension. Additionally, Dim_Crime is linked to Fact_Incidents, and Dim_Rental to Fact_RentalAmount.

This hybrid model enables efficient data retrieval while maintaining a clear representation of relationships across business entities.

<a href="https://github.com/utkarshdatawhiz993/Bus-Matrix-and-Data-Modeling/blob/main/Screenshot%202025-07-31%20at%2011.50.39%20AM.png"> Click here for model design</a>

