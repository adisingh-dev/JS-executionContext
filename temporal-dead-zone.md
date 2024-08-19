# what is temporal dead zone? 💀
✅ TDZ is the duration since let variables are hoisted till it is initialized a value. It is a separate space where let variables are allocated undefined in the memory component 
till the time they get initialized. Inside a block (e.g., {}, if, for, while), variables declared with let or const have a TDZ that is part of the block's execution context.In
Chrome DevTools, when you inspect such a block, the TDZ is denoted within that specific block scope

# for which variables TDZ is valid? 🤔
✅ for variables declared with const and let but not initialized

# what happens if we try to access a variable inside TDZ? 😵
✅ we get a ReferenceError saying "cannot access x before initialization". means we cannot access the variables in the TDZ and can only be accessed once some value is assigned to it

# what are the main differences b/w var and let/const? 😁
✅ let/const variables are stored in a separate memory space aka TDZ and cannot be accessed before initialization whereas var variables are stored in the memory component of current EC and
can be accessed without initialization<br>
✅ let/const are the latest es6 features while var is the old es5 feature<br>
✅ let/const variables are block scoped while var variables are function scoped<br>
✅ let/const variables cannot be redeclared, whole code will be ignored and SyntaxError will be thrown while var variables can be redeclared<br>
✅ let/const variables are not attached to global window object while var variables are by default attached to global window object

# are variables declared with let/const hoisted? 😛
✅ yes they are hoisted. but we cannot access them directly nor we'll get undefined unlike var variables because they are placed in a separate memory space reseved for the current block aka TDZ

# how we can avoid TDZ and unexpected undefined errors? 🧐
✅ the idea is to shrink the TDZ window to 0. To achieve this put all the variable declarations and declarations at the top of the current scope. with this we ensure that code first encounters these variables before trying to access them

# when do we get SyntaxError, ReferenceError and TypeError in JS?
✅ ReferenceError: while trying to access variables in TDZ or before declaration
✅ SyntaxError: while trying to declare let variables again and missed initialization while declaring const variables
✅ TypeError: while reinitializing const variables
