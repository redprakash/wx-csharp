# Language Integrated Query (LINQ) (C#)
- https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries
# LINQ CheatSheet
[LINQ CheatSheet.pdf](https://github.com/redprakash/wx-csharp/files/9131020/LINQ.CheatSheet.pdf)

# All LINQ query operations consist of three distinct actions:
  1. Obtain the data source.
  2. Create the query.
  3. Execute the query.
![image](https://user-images.githubusercontent.com/11143215/179476743-2e6625d2-b40a-4d88-bd0d-9c8a52ac2510.png)

# Advantages of LINQ
- LINQ is strongly typed
- LINQ can be used to transform the data into a different format
- Uses known C# language constructs
- Deferred execution

# LINQ Query Syntax
- The steps of getting the data source, writing the query and executing that query is LINQ query syntax
- Refer the above example

# LINQ Method Syntax
- Here rest is same as of Query Syntax except we use extension methods like (Where) instead of query
![image](https://user-images.githubusercontent.com/11143215/179482222-893bf7c2-2395-437c-b972-9d0d28ed27df.png)
    
    The function(here we have used lambda expression) inside Where is called predicate
    predicate => A function to test each element for a condition.

# Types of LINQ Operators
    Refer to the cheatsheet attached
