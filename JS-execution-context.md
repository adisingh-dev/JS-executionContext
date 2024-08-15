# What is JS?
JS is a synchronous single threaded language ie. JS executes one cmd at a time and executes next line when current line has finished executing

# What is Execution Context?
an execution context is a container in which whole JS code is executed. everything in JS happens inside execution context

# Components of execution context
1. Memory component/variable environment: it is an environment where variables and functions are stored as key-value pairs. all variables are assigned undefined values and variables with function names are created which literally store the whole function code as it is. The undefined values get replaced with the returned values from code component
2. Code component/thread of execution: it is a component in which a single thread executes the code one line at a time. When return statement is encountered the current EC is popped out of call stack and control goes back to function invocation and value is assigned to the caller variable. JS finds the final returned value in the memory component when it encounters return statement in the code component

# Call stack
whenever an EC is created it gets pushed into call stack and when it finish executing it gets popped out of the stack. GEC always gets pushed first in the call stack before going to the memory phase of GEC
