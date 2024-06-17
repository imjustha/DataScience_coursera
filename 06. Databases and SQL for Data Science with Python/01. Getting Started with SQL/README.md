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
Let's look at these codes in action. Below is a database table called 'COUNTRY,' which contains the columns ID, Name, and CCode. Here, CCode is a 2 letter country code.


   
