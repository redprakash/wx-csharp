# Topics
## .NET Framework vs .NET Core vs .NET vs .NET Standard vs C#
## What is architecture of .net core (i.e. how program/code executes on .net core platform)
## Explain how C# .net core framework works.
  - https://www.youtube.com/watch?v=4olO9UjRiww
## The Common Language Runtime (CLR)
  ``` The Common Language Runtime (CLR) is an Execution Environment . It works as a layer between Operating Systems and the applications written in .Net languages that conforms to the Common Language Specification (CLS). The main function of Common Language Runtime (CLR) is to convert the Managed Code into native code and then execute the Program. The Managed Code compiled only when it needed, that is it converts the appropriate instructions when each function is called . The Common Language Runtime (CLR) 's Just In Time (JIT) compilation converts Intermediate Language (MSIL) to native code on demand at application run time.```
  - http://vb.net-informations.com/framework/common_language_runtime.htm

## What is  Microsoft Intermediate Language (MSIL) 
  ``` MSIL stands for Microsoft Intermediate Language. We can call it as Intermediate Language (IL) or Common Intermediate Language (CIL). During the compile time , the compiler convert the source code into Microsoft Intermediate Language (MSIL) .Microsoft Intermediate Language (MSIL) is a CPU-independent set of instructions that can be efficiently converted to the native code. During the runtime the Common Language Runtime (CLR)'s Just In Time (JIT) compiler converts the Microsoft Intermediate Language (MSIL) code into native code to the Operating System. ```
  - http://vb.net-informations.com/framework/microsoft_intermediate_language.htm

## Just In Time Compiler - JIT
  ``` The .Net languages , which is conforms to the Common Language Specification (CLS), uses its corresponding runtime to run the application on different Operating Systems . During the code execution time, the Managed Code compiled only when it is needed, that is it converts the appropriate instructions to the native code for execution just before when each function is called. This process is called Just In Time (JIT) compilation, also known as Dynamic Translation . With the help of Just In Time Compiler (JIT) the Common Language Runtime (CLR) doing these tasks. ```
  - http://vb.net-informations.com/framework/just_in_time_compiler.htm

## What is compiled vs interpreted vs Hybrid language
  - https://www.youtube.com/watch?v=I1f45REi3k4

## Object Oriented Programming concepts (with C#)
  - https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop
  - `OOP Crash Course `
      - https://www.youtube.com/watch?v=SiBw7os-_zI
  - `OOP Concepts in C#`
      - https://www.youtube.com/watch?v=hxIb99-Z8_I
      - https://www.c-sharpcorner.com/UploadFile/84c85b/object-oriented-programming-using-C-Sharp-net/

  - `A static class is declared using the "static" keyword. If the class is declared as static then the compiler never creates an instance of the class. All the member fields, properties and functions must be declared as static and they are accessed by the class name directly not by a class instance object.`
  - `Interface`
      - https://www.programiz.com/csharp-programming/interface

## Get started with ASP.NET Core MVC
  ### Models: 
        - Classes that represent the data of the app.
        - The model classes use validation logic to enforce business rules for that data.
        - Typically, model objects retrieve and store model state in a database.
          
  ### Views: 
       - Views are the components that display the app's user interface (UI). Generally, this UI displays the model data.
 
 ### Controllers: Classes that:
       - Handle browser requests.
       - Retrieve model data.
       - Call view templates that return a response.
 - https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?WT.mc_id=dotnet-35129-website&view=aspnetcore-6.0&tabs=visual-studio

## C#/ASP .net core Web API basic understanding
  - https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-6.0&tabs=visual-studio

## Dependency injection in .net core
  `A dependency is an object that another object depends on`
  - https://docs.microsoft.com/en-us/dotnet/core/extensions/dependency-injection
  - https://www.youtube.com/watch?v=YR6HkvNBpX4
  - https://www.youtube.com/watch?v=daYmMZ28-Y0
  - https://www.c-sharpcorner.com/blogs/what-is-dependency-injection-and-what-are-its-types2

## MongoDb demo application using C#
  - https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mongo-app?view=aspnetcore-6.0&tabs=visual-studio

## Basic data structure problems
`Data Structures are a specialized means of organizing and storing data in computers in such a way that we can perform operations on the stored data more efficiently.`
  - https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42

## SQL server, T-SQL
`T-SQL stands for Transact Structure Query Language which is a Microsoft product and is an extension of SQL Language.`
  - https://www.tutorialspoint.com/t_sql/index.htm
  - https://www.youtube.com/watch?v=8hqpa5VF09Y
  - https://searchdatamanagement.techtarget.com/definition/T-SQL
  - https://www.sqlservertutorial.net/getting-started/what-is-sql-server/
 ### Tutorial: Writing Transact-SQL Statements
  - https://docs.microsoft.com/en-us/sql/t-sql/tutorial-writing-transact-sql-statements?view=sql-server-ver15

## Integration tests vs Unit tests vs End to end tests in asp.net core API
 ### Unit Testing (xUnit)
   - https://www.youtube.com/watch?v=dsD0CMgPjUk&t=15s
   - https://www.lambdatest.com/blog/nunit-vs-xunit-vs-mstest/
   - https://www.programmingwithwolfgang.com/xunit-getting-started/
 ### Fluent Assertions
    - https://fluentassertions.com/introduction

## SDLC
  - https://stackify.com/what-is-sdlc/

## WaterFall Model and Agile
  - https://www.atlassian.com/agile
  - https://www.projectmanager.com/waterfall-methodology

## Domain Driven Design
  - https://vaadin.com/learn/tutorials/ddd/tactical_domain_driven_design
  - https://github.com/dotnet-architecture/eShopOnContainers/tree/dev/src/Services/Ordering
  - https://leanpub.com/theanatomyofdomain-drivendesign

## Git/source control
  - https://www.perforce.com/blog/vcs/what-source-control

## Language Integrated Query (LINQ) (C#)
  ### Try LINQ
      - https://github.com/dotnet/try-samples
  - https://www.javatpoint.com/linq-min-function
  - https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/
  #### All LINQ query operations consist of three distinct actions:
      - Obtain the data source.
      - Create the query.
      - Execute the query.
## Azure DevOps
  - https://www.pluralsight.com/courses/continuous-delivery-azure-devops-big-picture
  - https://azure.microsoft.com/en-au/overview/devops-tutorial/#understanding

## LOGGING in ASP.NET Core
  - https://www.youtube.com/watch?v=dxBlBltEDRs

## 10 Exception handling best practices in C#
  ` An exception is a runtime error in a program that violates a system or application constraint, or a condition that is not expected to occur during the normal execution of       the program.`
  - https://kumarashwinhubert.com/10-exception-handling-best-practices-in-csharp

## LAMBDA
  - https://www.youtube.com/watch?v=DSxjciDUBdw

## Collections in C#
  - https://www.c-sharpcorner.com/UploadFile/736bf5/collection-in-C-Sharp/#:~:text=C%23%20collection%20types%20are%20designed,inserting%20items%20to%20a%20collection
  - https://www.tutorialspoint.com/csharp/csharp_collections.htm



## Repository Pattern in C#
     Repository Design Pattern acts as a middleman or middle layer between the rest of the application and the data access logic. 
     That means a repository pattern isolates all the data access code from the rest of the application. 
     The advantage of doing so is that, if you need to do any changes then you need to do it in one place. 
     Another benefit is that testing your controllers becomes easy because the testing framework need not run 
     against the actual database access code.
    
     A repository is nothing but a class defined for an entity, with all the possible database operations. 
     For example, a repository for an Employee entity will have the basic CRUD operations 
     and any other possible operations related to the Employee entity.
    
   - https://dotnettutorials.net/lesson/repository-design-pattern-csharp/

  ### Generic & Non Geneeric Repository Pattern in C#
   - https://dotnettutorials.net/lesson/generic-repository-pattern-csharp-mvc/
 
  ### Unit of Work in C# Repository Pattern
     The Unit of Work pattern is used to group one or more operations (usually database CRUD operations) into a single transaction 
     or “unit of work” so that all operations either pass or fail as one unit. In simple words we can say that for a specific user 
     action,say booking on a website, all the transactions like insert/update/delete and so on are done in one single transaction, 
     rather than doing multiple database transactions. This means, one unit of work here involves insert/update/delete operations, 
     all in one single transaction so that all operations either pass or fail as one unit.
      
      
   - https://dotnettutorials.net/lesson/unit-of-work-csharp-mvc/



# NOTES
` (MVC and Conosle) tutorial end to end thoroughly understood `
