# C#
    It is a general purpose programming language for mainly used for development of console apps,
    Windows GUI and Windows Services. It is strongly tped language. It is compiler based language
### Components of CLR (Common Language Runtime)
`It is Run Time Engine that is used to execute applications`
  - Class Loader -> (Loading classes from compiled source code to memory)
  - Memory Manager -> (Allocating necessary memory for objects )
  - Garbage Collector -> (Freeing/deleting memory of objects)
  - Just-In-Time (JIT) Compiler -> Convert Intermediate Language(IL) Code to Native Machine Language 
  - Exception Manager -> Raise notifications while run-time eroors, Creates Exception logs
  - Thread Manager -> Create threads (background process) to execute the code
  - Security Manager -> Verifies whether the application has permission to acces system resources or not
### What is Assembly
    A single unit of deployment
- https://www.youtube.com/watch?v=lx2tSY4joDg
### .NET Framework
` A platform to build different types of applications `

### .NET Framework Architecture

![dotnetframeworkarchitecture](https://user-images.githubusercontent.com/11143215/157343280-d06492a8-9de2-4b24-be6f-93b13005f0fe.PNG)

### Base Class Library (BCL)
    Contains a set of pre-defined classes that can be used in all types of .net applications & langugages for general
    I/O operations, type conversion, creation of threads etc.
    Examples, Console, String, Thread, Task classes

### ADO .NET
    Contains a set of pre-defined classes that can be used in all types of .net applications and languuages for connection 
    to databases, retrieving data from databases, inserting, updating, deleting rows etc.
    Examples: SqlConnection, Sql Command, SqlDataReader, SqlDataAdapter etc
    
### ASP .NET
    ASP.NET is a popular web-development framework for building web apps on the .NET platform.

### ASP .NET CORE
    ASP.NET Core is the open-source version of ASP.NET, that runs on macOS, Linux, and Windows.
    ASP.NET Core was first released in 2016 and is a re-design of earlier Windows-only versions of ASP.NET.
    
### Common Language Specifications
    Contains a set of rules /concepts that are common to all.net langugaes such as C#.NET, VB.NET etc
    
    
### Class
    It is a model of objects. Class (also known as "type") represents structure of data that you want to store in objects.

### Namespace
    namespace is grouping classes that are meant for specific purpose.
    Ex: If we have classes like, Student, Professors, Staffs then it can be grouped under `university` namespace
    
### C# Naming Conventions
  #### camelCase
        - For all local variables, parameters
        - Ex: customerName
  #### PascalCase
        - For all class names, structure names, namespace names, filed names, method names, property names
        - ex: CustomerName
  #### IPascalCase
        - For all interfaces names
        - Ex: ICustomerName
  #### _camelCase
        - For all private fields
        - Ex: _customerName

### Primitive Types
        - Strictly stores single values
        - Ex: sbyte,byte,shore,int,long,float,double,decimal,char,bool
### Non-Primite Types
        - Stores one or more values
        - Usually contains multiple members
        - Ex: string,Classes,Interfaces,Structures,Enumerations
    
 ### Heap  vs Stack
        - Objects are stored inside the `Heap`
        - For each method call a new stack call will be created
        
 - https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/

### Constant vs Readonly vs Static Keywords in C#
- https://www.c-sharpcorner.com/UploadFile/2072a9/constant-vs-readonly-vs-static-keywords-in-C-Sharp/
 
 
### Parameter Modifiers
Specifies how the poarameter receives a value
    Types
        - Default [No Keyword]
        - ref
        - out / out declaration
        - in
        - params

- https://dev.to/rooktko/passing-parameters-with-modifiers-in-c-57ll

### Local Functions
    Local Functions are functions, to do some small process which is written inside a nethod
    Local functions are not part of the calss, they can't be called directly through reference variable
    Local function do not support "access modifiers" and "modifiers"
```
public void MethodName(param1,param2, ..)
{
    LocalFunctionName(); --<-- Calling the local functions
    ReturnDataType LocalFunctionName(param1,param2,..)
    {
        //Local function Body here
    }
}

```
### Static Local Functions
    Same as the local functions, only difference is, static local functions cannot access localvariables or parameters of containing method
    This is to avoid accidental access of local variables or parameters of containing method, inside the local function

```
public void MethodName(param1,param2,...)
{
     LocalFunctionName(); --<-- Calling the local functions
     static ReturnDataType LocalFunctionName(param1,param2,..)
    {
        //We cannot access local variables or parameters of containing method
    }
}
```

### Type Casting
    1. Implicit Casting : (from lower-numerical-type to higher numerical type ex: int -> long)
    2. Explicit Casting : (from higher numerical type to lower numerical type ex: long -> int)
    3. Parsing / TryParse : from string to numerical-type ex: numerical string-> integer or numerical string -> double
        Try parse checks the value before converting. 
    4. Conversion Methods : (from any primitve type to any primitive type)
         Syntax: type destinationVariable = Convert.ConversionMethod(SourceValue)

## Indexer
    It is a special member of a class, which contains set-accessor ang get-accessor to access a group of items/ elements
- https://www.tutorialsteacher.com/csharp/csharp-indexer
```
public class Car
{
    private string[] _brands = new string[]{"Skoda","Hyunda","haval"}
    public string this[int index]
    {
        set { this._brands[index] = value; }
        get { return _brands[index] }
    }
}
```













