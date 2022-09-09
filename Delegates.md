# Delegates
    - An object that know how to call a method (or a group of methods)
    - A reference to a function
    - Delegates are used to pass methods as arguments to other methods.
https://www.tutorialsteacher.com/csharp/csharp-delegates

### A delegate can be declared using the delegate keyword followed by a function signature
    [access modifier] delegate [return type] [delegate name]([parameters])
    Ex: public delegate void MyDelegate(string msg);
    
## C# - Func Delegate
    C# includes built-in generic delegate types Func and Action, so that you don't need to define custom delegates manually 
    in most cases.Func is a generic delegate included in the System namespace. It has zero or more input parameters 
    and one out parameter. 
    The last parameter is considered as an out parameter.
    
    namespace System
    {    
      public delegate TResult Func<in T, out TResult>(T arg);
    }
