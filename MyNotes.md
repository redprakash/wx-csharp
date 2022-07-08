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
    Same as the local functions, only difference is, static local functions cannot access localvariables or parameters 
    of containing method
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
### Sealed Classes and  Sealed Methods
    A sealed class, in C#, is a class that cannot be inherited by any class but can be instantiated.
    The design intent of a sealed class is to indicate that the class is specialized and there is no need to extend it to 
    provide any additional functionality through inheritance to override its behavior. A sealed class is often used to encapsulate 
    a logic that needs to be used across the program but without any alteration to it.
    
    The method that is defined in a parent class, if that method cannot be overridden under a child class, we call it a sealed method. 
    By default, every method is a sealed method because overriding is not possible unless the method is not declared as virtual 
    in the parent class. 
    If a method is declared as virtual in a class, any child class of it can have the right to override that method
    
- https://dotnettutorials.net/lesson/sealed-class-methods-csharp/


### Abstract Class
    An abstract class is a special type of class that cannot be instantiated. An abstract class is designed to be inherited 
    by subclasses that either implement or override its methods
    
- https://www.geeksforgeeks.org/c-sharp-abstract-classes/    
    
### Abstract Method
    An Abstract method is a method without a body. The implementation of an abstract method is done by a derived class. 
    When the derived class inherits the abstract method from the abstract class, it must override the abstract method. This requirment 
    is enforced at compile time and is also called dynamic polymorphism.

- https://dotnettutorials.net/lesson/abstract-class-abstract-methods-csharp/

### Partial Class
    A partial class is a special feature of C#. It provides a special ability to implement the functionality of a single class 
    into multiple files and all these files are combined into a single class file when the application is compiled. A partial class 
    is created by using a partial keyword. This keyword is also useful to split the functionality of methods, interfaces, 
    or structure into multiple files
```
public partial Clas_name  
{
        // code
}
```
### C# Enumerations Type - Enum
    In C#, an enum (or enumeration type) is used to assign constant names to a group of numeric integer values. 
    It makes constant values more readable, for example, WeekDays.Monday is more readable then number 0 when referring 
    to the day in a week.
- https://www.tutorialsteacher.com/csharp/csharp-enum



### Readonly strucutures
>Use readonly struct  in case of following
    - All fileds are readonly
    - All properties have only 'get' accessors(readonly properties)
    - There is a prameterized constructor that initializes all the fields
    - You dont want to allow to change any field or property of the structure
    - Methods can read fields, but cannot modify



### Boxing & Unboxing
   #### Boxing is the process of converting a value from "Value-Type Data Type" to Reference-Type Data Type", if compatible
   #### Unboxing is a process of converting a value from "reference-type Data Type to "Value-Type Data Type", if compatible
    Boxing and unboxing in C# allows developers to convert .NET data types from value type to reference type and vice versa. 
    Converting a value type to a reference type is called called boxing in C# and converting a reference type to a value type 
    is called unboxing in C#. 
    
- https://www.c-sharpcorner.com/article/boxing-and-unboxing-in-C-Sharp/   


### Generics
    Generics allow you to define the specification of the data type of programming elements in a class or a method, 
    until it is actually used in the program. In other words, generics allow you to write a class or method that can work with any data type.
  
- https://www.tutorialspoint.com/csharp/csharp_generics.htm

### Generic Constraints (restrictions on generic parameters)
    - where T:class
    - where T:struct
    - where T : ClassName
    - where T : InterfaceName
    - where T : new()
    
```
class ClassName<T> where T :class
{
    public T FieldName;
}
``` 
### Null coalescing operator
    It checks wheter the value is null or not
        > It returns left-hand-side operand if the value is not null
        > It returns the right-hand-side operand if the value is null
``` variableName ?? valueIfNull ```
    
### Null Propagation Operator
    The "Null Propagation Operator (?.) and (? [] ) checks the value of left-hand operand 
    whether it is null or not
        -> It returns the right-hand-side operand (property or method), if the value is not null
        -> It returns null, if the value is null
    It accesses the property or method, only if the reference variable is "not null", just returns "null", if reference variable is "null"
    
`referenceVariable?.fieldName; `
    


### Extension Methods
    It is a new feature that has been added in C# 3.0 which allows us to add new methods into a class without editing the 
    source code of the class i.e. if a class consists of a set of members in it and in the future if you want to add new methods 
    into the class, you can add those methods without making any changes to the source code of the class.
    
- https://dotnettutorials.net/lesson/extension-methods-csharp/
    

### Pattern Matching
    Pattern matching is the process of taking an expression and testing whether it matches certain criteria, such as 
    ‘being a specified type’ or ‘matching a specified constant value’. C# supports various different patterns
    
    It allows yu to declare a variable, while checking the data type (class) of a reference variable, and automatically 
    type-casts the reference variable into the specified data type (class)
```
if(referenceVaribale  is Class c1)
{
    c1.Property..
}
```
- https://www.c-sharpcorner.com/article/pattern-matching-in-c-sharp-7-0/
- https://endjin.com/blog/2022/02/pattern-matching-in-csharp
- https://timdeschryver.dev/blog/pattern-matching-examples-in-csharp#why-pattern-matching


### Delegates
    A delegate is a reference type variable that holds the reference to a method. The reference can be changed at runtime.
    There are three steps involved while working with delegates:

        1. Declare a delegate
        2. Set a target method
        3. Invoke a delegate
        
- https://www.tutorialspoint.com/csharp/csharp_delegates.htm
- https://www.tutorialsteacher.com/csharp/csharp-delegates

#### Delegate Syntax
``` [access modifier] delegate [return type] [delegate name]([parameters]) ```

### Tuple
    A tuple is a data structure that contains a sequence of elements of different data types. It can be used where you want to 
    have a data structure to hold an object with properties, but you don't want to create a separate type for it
    
- https://www.tutorialsteacher.com/csharp/csharp-tuple#:~:text=A%20tuple%20is%20a%20data,a%20separate%20type%20for%20it.


The following example creates a tuple with three elements:
```
Tuple<int, string, string> person = 
                        new Tuple <int, string, string>(1, "Steve", "Jobs");
```

### Yield Return
- https://www.youtube.com/watch?v=HRXkeaeImGs&list=PLKjV8hx8vwdiwd-5oOI212YSe1lBCYpuO&index=1&t=86s
- https://www.youtube.com/watch?v=AAz8q6dOCYk


### Exception Handling
    - DividedByZero
    - FormatException
    - IndexOutOfRangeException
    - NullReferenceException
    - ArgumentNullException
    - Custom Exceptions
    - Exception Logger
    - Stack trace

## C# 9 and 10 - New Features
- Top Level Statements
- File Scoped Namespaces
- Global Using
- Module Initializer
    - https://khalidabuhakmeh.com/module-initializers-in-csharp-9
- Nullable Reference Types
- Null Forgiving Operator
- Pattern Matching - Switch Expression Pattern
- Records


## Explore
 - Anonymous Types
 - Anonymous Arrays
 - Discards ( _ ) (skipping the value/s) 
 - Summary and Regions usage
 - LINQ extension methods
 - String ( https://www.udemy.com/course/c-sharp-oop-ultimate-guide-project-master-class/learn/lecture/29157312#overview )
 - Regular Expressions
 - System.IO namespace
 - Json Serialization





