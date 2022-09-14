# C# Lock (Thread Lock)
    The lock(obj) statement specifies that the following section of code cannot be accessed by more than one thread 
    at the same time in C#. The obj parameter inside the lock(obj) statement is an instance of the object class. 
    The lock(obj) statement provides an efficient way of managing threads in C#. If the code inside the lock(obj) is 
    accessed by one thread and another thread wants to access the same code, the second thread will have to wait 
    for the first thread to execute it. The lock(obj) statement ensures sequential execution of the specified section of code
- https://www.tutlane.com/tutorial/csharp/csharp-thread-lock
- https://www.delftstack.com/howto/csharp/lock-statement-in-csharp/
