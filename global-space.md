# what is Global Space?
Any code in JS which is not written inside function scope. ie. the code written at top level of a JS module

# what is window object?
Whenever a JS program is executed a global execution context is created and pushed into the call stack. Along with it a global object is created. This behaviour is same in all JS runtimes
and for browser this global object is called window. in case of nodejs this global object is an empty object {} as nodejs does not support any browser specific events and properties. 

# why variables declared at global scope are attached to window object in case of browser v8 engine and not in case of nodejs runtime?
In Nodejs each file is treated as a separate module. Variables declared at the top level in a file (outside any function) are scoped to that module, not attached to the global object. This design 
encourages modularity and avoids polluting the global namespace, making it easier to manage code and avoid conflicts between different modules

