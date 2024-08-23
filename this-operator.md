# what is this operator in JS?
✅ whenever an EC is created a global object is created along with it, even for a function's EC and with that global object, a this operator is also created which points to the global object itself
this operator behaves differently in different scenarios

# what is the global object in browser and in nodejs?
✅ browser: window object<br>
✅ nodejs: empty global object {}

# in which mode this substitution occurs?
✅ in non strict mode only

# what is this substitution?
✅ whenever the value of this operator is undefined/null then this will be replaced with globalObject only in non strict mode

# what is the difference b/w a fn and a method?
✅ when we make a fn a part of an object or when a fn is defined inside and object then the fn aka method of the object. whereas a fn is called a fn when it is defined in the global space without
any object's own method

# how does this keyword behaves inside a fn in strict and non strict mode?
✅ In a fn the value of this depends on strict / non strict mode<br>
✅ In non strict mode this substitution will occur<br>
✅ In strict mode the value of this depends on how this fn is called eg. if we call a fn x() then in strict mode this will be undefined but in case of window.x() this will point to window<br>
✅ In case of of an object calling one of its method then this will point to that object itself

# what is enclosing lexical context?
✅ lexical means where something is written in the code heirarchy. so lexical context is the component in the memory phase of the current EC that contains the reference to the parent's EC

# explain how arrow fn treats this keyword?
✅ the arrow fn dont hv the concept of this so this inside arrow fn points to the enclosing lexical context of the containing code. where the arrow fn is lexically enclosed. It will be treated as
if the arrow fn is not there in the code and instead of arrow fn a simple this operator is used which will point to the object itself

# give different values of this operator in different scenarios?
✅ global space: window<br>
✅ inside a fn: undefined in strict but in non strict mode this substitution will occur so it will point to window globalObject<br>
✅ inside a method: object itself if it is regular fn but it will point to the object's enclosing lexical environment where they are enclosed in case of arrow fn<br>
✅ inside an arrow fn: enclosing lexical context because arrow fn do not hv their own this binding
