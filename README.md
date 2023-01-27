# Crowdfunding_ETL
 
# Background

For the ETL mini project, you will practice building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After you transform the data, you'll create four CSV files and use the CSV file data to create an ERD and a table schema. Finally, you’ll upload the CSV file data into a Postgres database.

# Create the Category and Subcategory DataFrames

Create a Category DataFrame that has the following columns:

- A "category_id" column that is numbered sequential form 1 to the length of the number of unique categories.

- A "category" column that has only the categories.
Export the DataFrame as a category.csv CSV file.

Create a SubCategory DataFrame that has the following columns:

- A "subcategory_id" column that is numbered sequential form 1 to the length of the number of unique subcategories.

- A "subcategory" column that has only the subcategories.
Export the DataFrame as a subcategory.csv CSV file.

*These were done via list comprehension by splitting the existing categories & subcategories column.*

# Campaign DataFrame

Create a Campaign DataFrame that has the following columns:

* The "cf_id" column.
* The "contact_id" column.
* The “company_name” column.
* The "blurb" column is renamed as "description."
* The "goal" column.
* The "goal" column is converted to a float datatype.
* The "pledged" column is converted to a float datatype.
* The "backers_count" column.
* The "country" column.
* The "currency" column.
* The "launched_at" column is renamed as "launch_date" and converted to a datetime format.
* The "deadline" column is renamed as "end_date" and converted to a datetime format.
* The "category_id" with the unique number matching the “category_id” from the category DataFrame.
* The "subcategory_id" with the unique number matching the “subcategory_id” from the subcategory DataFrame.
* And, create a column that contains the unique four-digit contact ID number from the contact.xlsx file.

Then export the DataFrame as a campaign.csv CSV file.

# Create the Contacts DataFrame
Create a Contacts DataFrame that has the following columns:

* A column named "contact_id" that contains the unique number of the contact person.
* A column named "first_name" that contains the first name of the contact person.
* A column named "last_name" that contains the first name of the contact person.
* A column named "email" that contains the email address of the contact person

Then export the DataFrame as a contacts.csv CSV file.

Two options were given:

* Option 1: Use Pandas to create the DataFrame

* Option 2: Use regex to create the contacts DataFrame.

*Option 1 was chosen, iterating through each row in the contacts.xlsx and converting them into a python dictionary. Each dictionary was split between it's column name and values. First and Last names were split into their own columns and the DataFrame was cleaned up and exported to contacts.csv.*

# Create the Crowdfunding Database

1. Inspect the four CSV files, and then sketch an ERD of the tables.
2. Use the information from the ERD to create a table schema for each CSV file.
3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a SELECT statement for each table.
7. Import each CSV file into its corresponding SQL table.
8. Verify that each table has the correct data by running a SELECT statement for each

![ERD](https://github.com/Solarnite/Crowdfunding_ETL/blob/main/Crowdfunding_ERD.png)
(https://github.com/Solarnite/Crowdfunding_ETL/blob/25de57e22b7829187a72ea68bc047ae12f531904/crowdfunding_db_schema.sql#L1-L65)
