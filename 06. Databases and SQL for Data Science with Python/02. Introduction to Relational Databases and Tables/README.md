# Introduction to Relational Databases and Tables

## Examples to ALTER and TRUNCATE tables using MySQL

### ALTER TABLE

ALTER TABLE statements can be used to add or remove columns from a table, to modify the data type of columns, to add or remove keys, and to add or remove constraints. The syntax of the ALTER TABLE statement is:

#### ADD COLUMN syntax
```sql
ALTER TABLE table_name
ADD column_name data_type;
```
A variation of the syntax for adding column is:
```sql
ALTER TABLE table_name
ADD COLUMN column_name data_type;
```
By default, all the entries are initially assigned the value `NULL`. You can then use `UPDATE` statements to add the necessary column values.

For example, to add a telephone_number column to the author table in the library database, the statement will be written as:
```sql
ALTER TABLE author 
ADD telephone_number BIGINT;
```
Here, BIGINT is a data type for Big Integer.
After adding the entries to the new column, a sample output is shown below.

![Screenshot 2024-06-17 at 4 07 49 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/9f935e1e-fb4a-4e39-acc5-10af5a0b8f6e)

#### Modify column data type
```sql
ALTER TABLE table_name
MODIFY column_name data_type;
```
Sometimes, the data presented may be in a different format than required. In such a case, we need to modify the data_type of the column. For example, using a numeric data type for telephone_number means you cannot include parentheses, plus signs, or dashes as part of the number. For such entries, the appropriate choice of data_type is CHAR.

To modify the data type, the statement will be written as:
```sql
ALTER TABLE author
MODIFY telephone_number CHAR(20);
```
The entries can then be updated using UPDATE statements. An updated version of the "author" table is shown below.

![Screenshot 2024-06-17 at 4 08 34 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/9ceb3858-56c8-4fa6-9c37-8e5231cb2fcf)

### TRUNCATE Table

TRUNCATE TABLE statements are used to delete all of the rows in a table. The syntax of the statement is:

```TRUNCATE TABLE table_name;```

So, to truncate the "author" table, the statement will be written as:

```TRUNCATE TABLE author;```
The output would be as shown in the image below.

![Screenshot 2024-06-17 at 4 09 16 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/28215fee-6f12-4ce0-a5a1-d25f676667b2)

## Examples to CREATE and DROP tables

### CREATE TABLE statement
In the previous video, we saw the general syntax to create a table:
```sql
CREATE TABLE TableName (
   COLUMN1 datatype,
   COLUMN2 datatype,
   COLUMN3 datatype, 
   ...
);
```

Consider the following examples:

1. Create a TEST table with two columns - ID of type integer and NAME of type varchar. For this, we use the following SQL statement.
```sql
CREATE TABLE TEST (
   ID int,
   NAME varchar(30)
);
```
2. Create a COUNTRY table with an integer ID column, a two-letter country code column, and a variable length country name column. For this, we may use the following SQL statement.
```sql
CREATE TABLE COUNTRY (
   ID int,
   CCODE char(2),
   Name varchar(60)
);
```
3. In the example above, make ID a primary key. Then, the statement will be modified as shown below.
```sql
CREATE TABLE COUNTRY (
   ID int NOT NULL,
   CCODE char(2),
   Name varchar(60)
   PRIMARY KEY (ID)
);
```
In the above example, the ID column has the NOT NULL constraint added after the datatype, meaning that it cannot contain a NULL or an empty value. This is added since the database does not allow Primary Keys to have NULL values.

### DROP TABLE

If the table you are trying to create already exists in the database, you will get an error indicating table XXX.YYY already exists. To circumvent this error, create a table with a different name or first DROP the existing table. It is common to issue a DROP before doing a CREATE in test and development scenarios.

The syntax to drop a table is:
```DROP TABLE TableName;```

For example, consider that you wish to drop the contents of the table COUNTRY if a table exists in the dataset with the same name. In such a case, the code for the last example becomes
```sql
DROP TABLE COUNTRY;
CREATE TABLE COUNTRY (
   ID int NOT NULL,
   CCODE char(2),
   Name varchar(60)
   PRIMARY KEY (ID)
);
```
WARNING: Before dropping a table, ensure it doesn't contain important data that can't be recovered easily.

Note that if the table does not exist and you try to drop it, you will see an error like XXX.YYY is an undefined name. You can ignore this error if the subsequent CREATE statement is executed successfully.

## SQL Scripts - Uses and Applications

### SQL Scripts

SQL scripts are a series of commands or a program that will be executed on an SQL server.

SQL scripts are useful for making complex database changes and can be used to create, modify, or delete database objects such as tables, views, stored procedures, and functions.

### Applications of SQL Scripts
Here are some of the things that you can do with SQL scripts:

- Create tables
  - You can use SQL scripts to create new tables in your database. This is useful when you need to add new functionality to your application or when you want to store new types of data.

- Drop tables
  - SQL scripts often have commands to Drop tables from databases. This is especially important before Create table commands to make sure that a table with the same name doesnt exist in the database already.

- Insert data
  - SQL scripts can also be used to insert data into your tables. This is useful when you need to populate your database with test data or when you want to import data from an external source.

- Update data
  - You can use SQL scripts to update existing data in your tables. This is useful when you need to correct errors or update records based on changing business requirements.

- Delete data
  - SQL scripts can also be used to delete data from your tables. This is useful when you need to remove old or obsolete records from your database.

- Create views
  - Views are virtual tables that allow you to query data from multiple tables as if they were a single table. You can use SQL scripts to create views that simplify complex queries and make it easier to work with your data.

- Create stored procedures
  - Stored procedures are precompiled SQL statements that can be executed on demand. You can use SQL scripts to create stored procedures that encapsulate complex business logic and make it easier to manage your database.

- Create triggers
  - Triggers are special types of stored procedures that are automatically executed in response to certain events, such as an insert, update, or delete operation. You can use SQL scripts to create triggers that enforce business rules and maintain data integrity.

### Example: Creating Tables

Let us execute a script containing the CREATE TABLE commands for all the tables in a given dataset, rather than create each table manually by typing the DDL commands in the SQL editor.

Note the following points about these scripts.

1. SQL scripts are basically a set of SQL commands compiled in a single file.
2. Each command must be terminated with a delimiter or terminator. Most often, the default delimiter is a semicolon `;`.
3. It is advisable to keep the extension of the file as `.sql`.
4. Upon importing this file in the phpMyAdmin interface, the commands in the file are run sequentially.
Consider the following script:
```sql
DROP TABLE IF EXISTS PATIENTS;
DROP TABLE IF EXISTS MEDICAL_HISTORY;
DROP TABLE IF EXISTS MEDICAL_PROCEDURES;
DROP TABLE IF EXISTS MEDICAL_DEPARTMENTS;
DROP TABLE IF EXISTS MEDICAL_LOCATIONS;

CREATE TABLE PATIENTS (
  PATIENT_ID CHAR(9) NOT NULL,
  FIRST_NAME VARCHAR(15) NOT NULL,
  LAST_NAME VARCHAR(15) NOT NULL,
  SSN CHAR(9),
  BIRTH_DATE DATE,
  SEX CHAR,
  ADDRESS VARCHAR(30),
  DEPT_ID CHAR(9) NOT NULL,
  PRIMARY KEY (PATIENT_ID)
);

CREATE TABLE MEDICAL_HISTORY (
  MEDICAL_HISTORY_ID CHAR(9) NOT NULL,
  PATIENT_ID CHAR(9) NOT NULL,
  DIAGNOSIS_DATE DATE,
  DIAGNOSIS_CODE VARCHAR(10),
  MEDICAL_CONDITION VARCHAR(100),
  DEPT_ID CHAR(9),
  PRIMARY KEY (MEDICAL_HISTORY_ID)
);

CREATE TABLE MEDICAL_PROCEDURES (
  PROCEDURE_ID CHAR(9) NOT NULL,
  PROCEDURE_NAME VARCHAR(30),
  PROCEDURE_DATE DATE,
  PATIENT_ID CHAR(9) NOT NULL,
  DEPT_ID CHAR(9),
  PRIMARY KEY (PROCEDURE_ID)
);

CREATE TABLE MEDICAL_DEPARTMENTS (
  DEPT_ID CHAR(9) NOT NULL,
  DEPT_NAME VARCHAR(15),
  MANAGER_ID CHAR(9),
  LOCATION_ID CHAR(9),
  PRIMARY KEY (DEPT_ID)
);

CREATE TABLE MEDICAL_LOCATIONS (
  LOCATION_ID CHAR(9) NOT NULL,
  DEPT_ID CHAR(9) NOT NULL,
  LOCATION_NAME VARCHAR(50),
  PRIMARY KEY (LOCATION_ID, DEPT_ID)
);
```
This script incorporates commands to first drop any tables with the mentioned names in the database. After that, the script contains commands to create 5 different tables. All these commands are executed sequentially on the interface.

The contents of this file can be saved in a `.sql` file format and executed on the phpMyAdmin interface. This can be done by first selecting the database, uploading the SQL script in the provided space, and executing it, as shown in the image below.

![Screenshot 2024-06-17 at 4 15 10 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/474eea54-5361-47ed-9bd1-37da354e2b83)

Upon successful execution of each statement in sequence, an note appears on the interface as shown in the image below. It is also prudent to note that the tables created are now visible in the tree structure on the left under the selected database.

![Screenshot 2024-06-17 at 4 15 28 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/f4ed8bdc-e3d3-428c-88de-e768a6748781)

You may click any of the tables to see its Table Definition (its list of columns, data types, and so on). The image below displays the structure of the table PATIENTS.

![Screenshot 2024-06-17 at 4 15 39 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/937ac3ba-0fc6-45d9-b2ee-9044e3fae97a)


## SQL Cheat Sheet: CREATE TABLE, ALTER, DROP, TRUNCATE


![Screenshot 2024-06-17 at 4 16 35 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/3de04976-07a4-429b-bdbd-1a2f9c05dfac)
