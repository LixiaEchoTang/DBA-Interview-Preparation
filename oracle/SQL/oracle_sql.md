`**Date:** March 13, 2025`

# 1. Retrieve Data using the SQL SELECT Statement

## Top 5 Interview Questions
- What is the purpose of the SELECT statement in SQL?
- How do you differentiate between selecting all columns and specific columns?
- Explain the basic syntax of a SELECT statement.
- What role does the FROM clause play in a SELECT query?
- How do you use SELECT DISTINCT to eliminate duplicate rows?

## Core Concepts, Tools & Demos
- **Core Concepts:** SQL syntax, SELECT clause, FROM clause, use of DISTINCT
- **Tools:** Oracle SQL Developer, SQL*Plus
- **Demos:** Running simple queries to display entire tables versus specific columns

# 2. Restrict and Sort Data

## Top 5 Interview Questions
- How do you filter data using the WHERE clause?
- What is the purpose of the ORDER BY clause, and how does it work?
- How can multiple conditions be combined in a WHERE clause?
- What is the difference between ascending and descending order?
- How do you manage NULL values in sorting?

## Core Concepts, Tools & Demos
- **Core Concepts:** WHERE clause, logical operators, ORDER BY clause
- **Tools:** Oracle SQL Developer
- **Demos:** Filtering data with multiple conditions and sorting results in both ascending and descending order

# 3. Customize Output Using Single-Row Functions

## Top 5 Interview Questions
- What are single-row functions and why are they useful?
- How do you use string functions like UPPER, LOWER, or SUBSTR?
- Explain the use of numeric functions in Oracle SQL.
- How can date functions transform data outputs?
- Can you show an example where a single-row function is used to format data?

## Core Concepts, Tools & Demos
- **Core Concepts:** String, numeric, and date functions; data transformation
- **Tools:** Oracle SQL Developer
- **Demos:** Converting text cases and formatting dates within query outputs

# 4. Use Conversion Functions and Conditional Expressions

## Top 5 Interview Questions
- What is the purpose of conversion functions in Oracle SQL?
- How does the TO_CHAR function assist in formatting dates and numbers?
- What are conditional expressions, and when would you use a CASE statement?
- How does the DECODE function work as an alternative to CASE?
- Can you provide an example of converting a numeric value to a string using conversion functions?

## Core Concepts, Tools & Demos
- **Core Concepts:** Data type conversion, CASE and DECODE expressions
- **Tools:** Oracle SQL Developer
- **Demos:** Converting data types and applying conditional logic in queries

# 5. Report Aggregated Data Using the Group Functions

## Top 5 Interview Questions
- What are aggregate functions and how do they work?
- Explain the role of the GROUP BY clause in aggregation.
- How do you use the HAVING clause to filter aggregated data?
- What is the difference between COUNT(*) and COUNT(column_name)?
- Can you give an example of summarizing data with SUM or AVG?

## Core Concepts, Tools & Demos
- **Core Concepts:** Aggregation, GROUP BY, HAVING clause, COUNT, SUM, AVG
- **Tools:** Oracle SQL Developer
- **Demos:** Creating summary reports by grouping data and filtering groups

# 6. Display Data from Multiple Tables Using Joins

## Top 5 Interview Questions
- What are the different types of joins in Oracle SQL?
- How do you differentiate between an inner join and an outer join?
- Describe the ANSI join syntax versus the Oracle join syntax.
- What is a self join and when might you use one?
- How do join conditions affect the query result?

## Core Concepts, Tools & Demos
- **Core Concepts:** INNER, LEFT/RIGHT (outer), CROSS, and self joins; join conditions
- **Tools:** Oracle SQL Developer
- **Demos:** Joining two or more tables and exploring the differences between join types

# 7. Using Subqueries to Solve Queries

## Top 5 Interview Questions
- What is a subquery and how does it differ from a join?
- Explain the difference between correlated and non-correlated subqueries.
- How can subqueries be used in the WHERE clause?
- What are the benefits and drawbacks of using subqueries?
- Can you provide an example where a subquery is used in the SELECT clause?

## Core Concepts, Tools & Demos
- **Core Concepts:** Subquery structure, correlated vs. non-correlated, nesting queries
- **Tools:** Oracle SQL Developer
- **Demos:** Writing queries that incorporate subqueries to filter or compute results

# 8. Using Set Operators

## Top 5 Interview Questions
- What are set operators and why are they important in SQL?
- How does UNION differ from UNION ALL?
- Explain the roles of INTERSECT and MINUS in combining query results.
- What are the prerequisites for using set operators on multiple queries?
- Can set operators be nested, and if so, how?

## Core Concepts, Tools & Demos
- **Core Concepts:** UNION, UNION ALL, INTERSECT, MINUS; set theory in SQL
- **Tools:** Oracle SQL Developer
- **Demos:** Merging result sets from separate queries using various set operators

# 9. Manage Tables by Using DML Statements

## Top 5 Interview Questions
- What is the difference between DML and DDL?
- How do you insert new records into a table using the INSERT statement?
- What is the syntax for updating existing records?
- How do you safely delete records using the DELETE statement?
- What roles do COMMIT and ROLLBACK play in DML operations?

## Core Concepts, Tools & Demos
- **Core Concepts:** INSERT, UPDATE, DELETE, transaction control
- **Tools:** Oracle SQL Developer, SQL*Plus
- **Demos:** Executing DML commands and demonstrating transaction management with commit and rollback

# 10. Introduction to Data Definition Language

## Top 5 Interview Questions
- What does DDL stand for and what operations does it cover?
- How does DDL differ from DML in terms of impact on data?
- What is the syntax for creating a table using DDL?
- How do you modify an existing table structure with ALTER?
- What are the consequences of dropping a table using DROP?

## Core Concepts, Tools & Demos
- **Core Concepts:** CREATE, ALTER, DROP; schema definition and changes
- **Tools:** Oracle SQL Developer
- **Demos:** Creating and altering table structures and explaining the impact on the database schema

# 11. Introduction to Data Dictionary Views

## Top 5 Interview Questions
- What are data dictionary views and why are they important?
- How do DBA, ALL, and USER views differ?
- How can you query the data dictionary to obtain metadata about objects?
- What kind of information can you extract from data dictionary views?
- Can you provide an example of querying a specific data dictionary view?

## Core Concepts, Tools & Demos
- **Core Concepts:** Data dictionary, system metadata, DBA/ALL/USER views
- **Tools:** Oracle SQL Developer
- **Demos:** Querying the data dictionary to display details about tables, indexes, and other objects

# 12. Create Sequences, Synonyms, Indexes, Views, and Schema Objects

## Top 5 Interview Questions
- What is a sequence in Oracle and how is it used?
- How do you create and use synonyms in Oracle?
- Explain how indexes can improve query performance.
- What are the benefits of using views over tables?
- How do you manage schema objects with DDL commands?

## Core Concepts, Tools & Demos
- **Core Concepts:** Sequences, synonyms, indexes, views, and overall schema management
- **Tools:** Oracle SQL Developer
- **Demos:** Creating sequences for auto-increment, building synonyms for object aliasing, and demonstrating index creation and view management

# 13. Retrieving Data by Using Subqueries

## Top 5 Interview Questions
- How does using a subquery in the SELECT clause differ from the WHERE clause?
- What are the advantages of using subqueries for data retrieval?
- How can you nest multiple subqueries in a single query?
- What are the performance implications of subqueries?
- Can you illustrate a scenario where a subquery is essential for data retrieval?

## Core Concepts, Tools & Demos
- **Core Concepts:** Advanced subquery usage, nesting, and optimization
- **Tools:** Oracle SQL Developer
- **Demos:** Implementing queries that use subqueries to retrieve data from related datasets

# 14. Manipulating Data by Using Subqueries

## Top 5 Interview Questions
- How can you incorporate subqueries within DML statements?
- Provide an example where a subquery is used in an UPDATE statement.
- What are some common pitfalls when using subqueries in DELETE statements?
- How do subqueries help maintain data integrity during manipulation?
- How can you troubleshoot performance issues related to subqueries in DML operations?

## Core Concepts, Tools & Demos
- **Core Concepts:** Combining DML operations with subqueries, ensuring data consistency
- **Tools:** Oracle SQL Developer
- **Demos:** Updating and deleting records where conditions are determined via subqueries

# 15. Manage Data by Using Subqueries and Advanced Queries

## Top 5 Interview Questions
- What defines an advanced query in Oracle SQL?
- How do you integrate subqueries with analytical functions?
- What techniques can optimize complex subquery-based queries?
- How do you combine multiple subqueries to solve intricate data problems?
- Can you walk through a comprehensive example of an advanced query?

## Core Concepts, Tools & Demos
- **Core Concepts:** Advanced querying, performance tuning, integration of subqueries with analytical functions
- **Tools:** Oracle SQL Developer
- **Demos:** Constructing a complex query that leverages subqueries and advanced SQL features for data analysis

# 16. Control User Access and Manage Data in Different Time Zones

## Top 5 Interview Questions
- How are user privileges and roles managed in Oracle Database?
- What is the difference between granting a role versus granting a privilege?
- How can you restrict user access to specific tables or data?
- What are the best practices for handling time zone data in Oracle?
- How do you ensure data security and integrity across different time zones?

## Core Concepts, Tools & Demos
- **Core Concepts:** User management, role-based access control, time zone support, security best practices
- **Tools:** Oracle SQL Developer, Oracle Enterprise Manager
- **Demos:** Creating users, assigning roles/privileges, and configuring time zone–aware data fields
