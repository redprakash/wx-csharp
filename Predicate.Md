# Predicate

    Predicate in general meaning is a statement about something that is either true or false. 
    In programming, predicates represent single argument functions that return a boolean value.


    Predicate is the delegate like Func and Action delegates. It represents a method containing a set of criteria and 
    checks whether the passed parameter meets those criteria. A predicate delegate methods must take one input parameter 
    and return a boolean - true or false.

 - https://www.tutorialsteacher.com/csharp/csharp-predicate

 ## Example
    static bool IsUpperCase(string str)
    {
        return str.Equals(str.ToUpper());
    }

    static void Main(string[] args)
    {
        Predicate<string> isUpper = IsUpperCase;
        bool result = isUpper("hello world!!");
        Console.WriteLine(result);
    }
    Output = false

## An anonymous method can also be assigned to a Predicate delegate type as shown below.
    static void Main(string[] args)
    {
        Predicate<string> isUpper = delegate(string s) { return s.Equals(s.ToUpper());};
        bool result = isUpper("hello world!!");
    }
    
## A lambda expression can also be assigned to a Predicate delegate type as shown below.
    static void Main(string[] args)
    {
        Predicate<string> isUpper = s => s.Equals(s.ToUpper());
        bool result = isUpper("hello world!!");
    }
    
    
    
