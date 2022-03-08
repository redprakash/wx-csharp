#  Structured Query Language
  - https://www.w3schools.com/sql/sql_intro.asp#:~:text=SQL%20stands%20for%20Structured%20Query,for%20Standardization%20(ISO)%20in%201987

# JOINS
  - https://www.youtube.com/watch?v=0OQJDd3QqQM

 ### Inner join is anyting that matches between two tables based on the `ON` condition

 ### Left Join = inner join + any additional records in the left table
 ### Right Join = inner join + any additional records in the right table
 ### Full Join = inner join + all remaining records from left table + all remaining records from right table
  
# Trigger
  An Event driben T-SQL Programming block which runs automatically when a particular event occurs
  ` create trigger [trigger_name] 
    [before | after]  
    {insert | update | delete}  
    on [table_name]  
    [for each row]  
    [trigger_body] `
    
  ### Insert, Update, Delete -> DML Command -> DML Trigger
  ### Create, Alter, Drop -> DDL Command -> DDL Trigger
  ## Logon triggers which fire in response to LOGON events
  - https://www.youtube.com/watch?v=loF5gP738YU
  - https://www.sqlservertutorial.net/sql-server-triggers/
  - https://www.geeksforgeeks.org/sql-trigger-student-database/#:~:text=Explanation%20of%20syntax%3A,This%20specifies%20the%20DML%20operation.
 
  
# VIEWS
  In SQL, a view is a virtual table based on the result-set of an SQL statement.A view contains rows and columns, 
  just like a real table. The fields in a view are fields from one or more real tables in the database.
  
 `
  CREATE VIEW view_name AS
    SELECT column1, column2,..
    FROM table_name
    WHERE condition; 
   `
    
# Recursive Queries
  A recursive common table expression (CTE) is a CTE that references itself. By doing so, 
  the CTE repeatedly executes, returns subsets of data, until it returns the complete result set.
  - https://www.sqlservertutorial.net/sql-server-basics/sql-server-recursive-cte/
  - https://docs.microsoft.com/en-us/sql/t-sql/queries/with-common-table-expression-transact-sql?view=sql-server-ver15
  
  ` WITH expression_name (column_list)
    AS
    (
        -- Anchor member
        initial_query  
        UNION ALL
        -- Recursive member that references expression_name.
        recursive_query  
    )
    -- references expression name
    SELECT *
    FROM   expression_name `
    
# Cursors (Transact-SQL)
  A database cursor is an object that enables traversal over the rows of a result set. It allows you to process individual row returned by a query.
  - https://www.sqlservertutorial.net/sql-server-stored-procedures/sql-server-cursor/
  ![image](https://user-images.githubusercontent.com/11143215/157333980-e8dbf2ef-8762-4c3d-896a-4121727f3272.png)

# SQL Stored Procedures
  A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.So if you have an SQL query 
  that you write over and over again, save it as a stored procedure, and then just call it to execute it.You can also pass parameters to a 
  stored procedure, so that the stored procedure can act based on the parameter value(s) that is passed.
  - https://www.w3schools.com/sql/sql_stored_procedures.asp
  - https://www.sqlservertutorial.net/sql-server-stored-procedures/
```CREATE PROCEDURE procedure_name
AS
sql_statement
GO;
```

    
    
