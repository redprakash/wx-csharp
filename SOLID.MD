# SOLID PRINCIPLES
<img width="1557" alt="SOLID" src="https://user-images.githubusercontent.com/11143215/156481834-ecd1ca25-64b9-43e3-9138-9818abf56854.PNG">



# Simple explanation with plain examples
- https://www.youtube.com/watch?v=9qvCeRt9_hM&list=PLKjV8hx8vwdhLLhfIHG-CGIC1vmRwBiCF&index=27
- https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898
# Single Responsibility Principle
    `Each software module should have one and only one reason to change`
      A module in C# could be classes and methods

   ### Class Coupling and Cohesion
    `If our module performs one task and nothing else or has a clear purpose, our module has high cohesion. On the other hand, 
    if our module tries to encapsulate more than one purpose or has an unclear purpose, our module has low cohesion.`
    
   #### Relationships between classes is coupling
   
# Open/Closed Principle
  `Software entities(classes,modules,functions, etc) should be open for extension, but closed for modification`
  ### Closed For Modification
    New features getting added to the software component, should NOT have to modify existing code
  
  ### Open For Extension
    A software component should be extendable to add a new feature or to add a new behavior to it.
  
# Liskov Substitution Principle
    Objects should be replaceable with their subtypes without affecting the correctness of the program

# Interface Segreagation Principle
    No clients should be forced to depend on methods it does not use
    
### Techniques to Identify Violations of ISP
1. Fat Interfaces: An interface with lots of methods

        public interface IMultifunction 
        {
            public void print();
            public void getPrintSpoolDetails();
            public void scan();
            public void scanPhoto();
            public void fac();
            public void internetFax();

        }
    
2. Interfaces with low cohesion
3. Empty or blank method implementations


# Dependency Inversion Principle
    High-level modules should not depend on low-level modules. Both should depend on abstractions.
    Abstractions should not depend on Details. Details should depend on Abstractions.
 
 
   
   
