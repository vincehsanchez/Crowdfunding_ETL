# Crowdfunding_ETL
### Instructions
The instructions for this mini project are divided into the following subsections:
- Create the Category and Subcategory DataFrames
- Create the Campaign DataFrame
- Create the Contacts DataFrame
- Create the Crowdfunding Database

### Create the Category and Subcategory DataFrames

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
A "category" column that contains only the category titles
<img width="190" alt="category_DataFrame" src="https://github.com/vincehsanchez/Crowdfunding_ETL/assets/141890646/cade9f66-294a-4034-9537-335ea842750b">

2. Export the category DataFrame as category.csv and save it to your GitHub repository.
3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
- A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
- A "subcategory" column that contains only the subcategory titles
<img width="250" alt="subcategory_DataFrame" src="https://github.com/vincehsanchez/Crowdfunding_ETL/assets/141890646/72d6f738-6fba-4002-be97-c03f240478ec">

4. Export the subcategory DataFrame as subcategory.csv and save it to your!
 GitHub repository.

### Create the Campaign DataFrame

1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
- The "cf_id" column
- The "contact_id" column
- The "company_name" column
- The "blurb" column, renamed to "description"
- The "goal" column, converted to the float data type
- The "pledged" column, converted to the float data type
- The "outcome" column
- The "backers_count" column
- The "country" column
- The "currency" column
- The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
- The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
- The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
- The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
<img width="1074" alt="campaign_DataFrame" src="https://github.com/vincehsanchez/Crowdfunding_ETL/assets/141890646/1a6e748b-9fb7-4406-9d2e-077d9048c064">

2. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

### Create the Contacts DataFrame

**Option 2: Use regular expressions**
- Import the contacts.xlsx file into a DataFrame.
- Extract the "contact_id", "name", and "email" columns by using regular expressions.
- Create a new DataFrame with the extracted data.
- Convert the "contact_id" column to the integer type.
- Split each "name" column value into a first and a last name, and place each in a new column.
- Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.
- Check that your final DataFrame resembles the one in the following image:
<img width="415" alt="contact_DataFrame_final" src="https://github.com/vincehsanchez/Crowdfunding_ETL/assets/141890646/4c8140aa-1b11-4cc4-9ebe-0f528d41fc69">

### Create the Crowdfunding Database

1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD Links to an external site..
2. Use the information from the ERD to create a table schema for each CSV file.
3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a SELECT statement for each table.
7. Import each CSV file into its corresponding SQL table.
8. Verify that each table has the correct data by running a SELECT statement for each.
