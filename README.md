# Crowdfunding_ETL

This project is aimed to get a better understanding of the ETL pipeline. In this project we built an ETL pipeline utilizing Python, Pandas, and Python dictionary methods to extract and transform the data. After this process, we created 4 CSV files and used the CSV files to create an ERD and a table schema. The CSV files were then uploaded into a PostGres database.

## Resources Used:

- [crowdfunding](https://github.com/didierduyha/Crowdfunding_ETL/blob/main/Resources/crowdfunding.xlsx)
- [contacts](https://github.com/didierduyha/Crowdfunding_ETL/blob/main/Resources/contacts.xlsx)


Softwares Utilized:

Jupyter Notebooks, Pandas, Numpy, PostGresSQL, QuickDBD, pgAdmin4

## Data Extraction and Transformation

File location for code: [ETL Mini Project](https://github.com/didierduyha/Crowdfunding_ETL/blob/main/ETL_Mini_Project_IEllahi_DHa.ipynb)

### Category DataFrames

- A DataFrame is created for categories.
- The DataFrame contains a "category_id" column with sequential entries from "cat1" to "catn" for unique categories.
- The DataFrame has a "category" column that contains only the category titles.
- The category DataFrame is exported as category.csv.

### Subcategory DataFrames

- A DataFrame is created for subcategories.
- The DataFrame contains a "subcategory_id" column with sequential entries from "subcat1" to "subcatn" for unique subcategories.
- The DataFrame contains a "subcategory" column that contains only the subcategory titles.
- The subcategory DataFrame is exported as subcategory.csv.

### Campaign DataFrame

- A DataFrame is created for campaigns.
- The DataFrame includes various columns such as "cf_id", "contact_id", "company_name", "description", "goal", "pledged", "outcome", "backers_count", "country", "currency", "launch_date", "end_date", "category_id", and "subcategory_id".
- The "launch_date" and "end_date" columns are formatted as "YYYY-MM-DD".
- The campaign DataFrame is exported as campaign.csv.

### Contacts DataFrame

- A DataFrame is created for contacts.
- The DataFrame includes columns for "contact_id", "first_name", "last_name", and "email".
- The contacts DataFrame is exported as contacts.csv.

# Crowdfunding Database

![Crowdfunding ERD Chart](https://github.com/didierduyha/Crowdfunding_ETL/assets/131824263/aacd4e98-acab-49e0-bb4b-c43c23de164f)


- Utilizing the 4 CSV files created, we created an ERD.
- We created a table schema for each CSV file (which includes the primary keys, foreign keys, and other constraints).
- The Database schema is created as a Postgres file named crowdfunding_db_schema.sql.
- A new Postgres database was created: crowdfunding_db with tables for campaign, category, subcategory, and contacts.
- We can import each CSV file into its corresponding SQL table.

# Usage

To run the ETL pipeline and populate the PostgreSQL database, follow these steps:

- Ensure you have Python and the required dependencies installed.
- Execute the Jupyter Notebook containing the ETL pipeline code.
- Verify that the CSV files (contacts, campaign, category, subcategory) are created, and the PostgreSQL database is populated.
- Utilize SELECT statements to retrieve and analyze the data from the database.
