# Debugging with Visual Studio
- https://www.youtube.com/watch?v=5CpVjfTx1vg
- https://www.youtube.com/watch?v=U_UGuxqi_3E


# Debugging tips and shortcuts
### F5 => Run the application in Debug mode
### Ctrl + F5 => Run without the Debug mode
### F9 => Adds and removes break point at that line
### F10 => Step Over
    An action to take in the debugger that will step over a given line. If the line contains a function the function will be executed 
    and the result returned without debugging each line.
### F11 => Step into the method to find whats happening in that method
    An action to take in the debugger. If the line does not contain a function it behaves the same as “step over” but if it does
    the debugger will enter the called function and continue line-by-line debugging there.
### Shift + F11 => Step Out
    An action to take in the debugger that returns to the line where the current function was called.
### F5 => Continue to the next breakpoint while in debug mode
### Debug -> windows -> Breakpoints => View all the breakpoints in the application
