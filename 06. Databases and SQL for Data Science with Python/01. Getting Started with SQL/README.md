# Basic SQL

## SELECT statement examples

### SELECT statement usage
SELECT is classified as a Database Query command used to retrieve information from a database table.

There are various forms in which a SELECT statement is used.

1. The general syntax of a SELECT statement retrieves the data under the listed columns from Table_1. The code is:
   ```
   SELECT COLUMN1, COLUMN2, ... FROM TABLE_1 ;
   ```
2. To retrieve all columns from a table, use " * " instead of specifying individual column names. The code below retrieves the entire table.
   ```
   SELECT * FROM TABLE_1 ;
   ```
3. Use the WHERE clause to filter the required data based on a predicate. The code below filters the response to only the entries that match the predicate.
   ```
   SELECT <COLUMNS> FROM TABLE_1 WHERE <predicate> ;
   ```

### SELECT examples
Let's look at these codes in action. Below is a database table called 'COUNTRY,' which contains the columns `ID`, `Name`, and `CCode`. Here, `CCode` is a 2 letter country code.

![Screenshot 2024-06-17 at 3 38 53 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/1d253e30-331f-4f65-813e-352a2414c11a)

#### Example #1
When we apply the `SELECT code SELECT * FROM COUNTRY ;`, the query retrieves all rows and columns from the database table named COUNTRY.

- 'SELECT *' instructs the database to select all columns from the table.
- 'FROM COUNTRY' specifies the table from which to retrieve the data. In this case, it's the "COUNTRY" table, so the entire table appears, as shown below.
Response:
![Screenshot 2024-06-17 at 3 39 41 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/e9e9ec68-97e4-4d75-ad31-2810f8f57fa4)

#### Example #2
The SQL query `SELECT ID, Name FROM COUNTRY ;` retrieves specific columns from a database table named 'COUNTRY'.

- 'SELECT ID, Name' instructs the database to select two specific columns from the table: "ID" and "Name." It will return these two columns for each row that matches the query criteria.
- 'FROM COUNTRY' specifies the table from which to retrieve the data, which is the "COUNTRY" table. The table below shows that only the "ID" and "CCode" columns were retrieved.
Response:
![Screenshot 2024-06-17 at 3 40 22 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/909122e5-2d1a-4ebd-8e68-eaa97f825a69)

#### Example #3
The SQL query `SELECT * FROM COUNTRY WHERE ID <= 5 ;` retrieves all columns from the "COUNTRY" table where the value in the "ID" column is less than or equal to 5.

- `SELECT * instructs the database to select all columns from the specified table.
- FROM COUNTRY specifies the table from which to retrieve the data, which is the 'COUNTRY' table.
- WHERE ID <= 5 ; is a condition that filters the rows from the table. It will only return rows where the value in the "ID" column is less than or equal to 5. In the table below, you can see that only rows 1-5 were retrieved.
Response:
![Screenshot 2024-06-17 at 3 41 02 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/47b5a406-add4-4b22-b34e-2e9499f1215d)

#### Example #4
The SQL query `SELECT * FROM COUNTRY WHERE CCode = 'CA' ;` retrieves all columns from the "COUNTRY" table where the value in the "CCode" column is equal to 'CA'.

- `SELECT * instructs the database to select all columns from the specified table.
- FROM COUNTRY specifies the bale from which to retrieve the data, which is the 'COUNTRY' table.
- WHERE CCode = 'CA'; is a condition that filters the rows from the table. It will only return rows where the value in the "CCode" column is equal to 'CA.' In the table below, you will find that only the CA column was retrieved.
Response:
![Screenshot 2024-06-17 at 3 41 44 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/770cf875-ecdc-431c-9a34-0854c4ff7480)

![Screenshot 2024-06-17 at 3 43 29 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/21fc550f-60aa-47b3-837c-3545ead36dce)
