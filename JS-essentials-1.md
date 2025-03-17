
## type conversion
equality (==) and comparison operators work differently. comparisons convert null to a number
ie. 0 that's why null >= 0 is true and rest are false also when undefined is compared to any datatype it always gives false
```Javascript
console.table([
    typeof null,  // object
    typeof undefined,  // undefined
    Number("10abc"),  // nan
    Number(null),  0
    Number(undefined),  // nan
    "1" + 2 + 2,  // "122"
    typeof 1 + 2 + "2"  // "32"
]);
console.table([
    null > 0,  false
    null == 0,  false
    null >= 0  true
]);
```

## primitive 7 types: 
Number, String, Boolean, null, undefined, Symbol, bigint

## reference (non primitive 3 types): 
Arrays, Objects, Functions

## memory: Stack(primitives), Heap(references)
shallow copy: share the reference, deep copy: dont share same reference

## imp methods
slice(array/string): returns new string (start, end] (arrays, strings)\
splice: deletes/adds a sub-string/array and returns deleted part (start, #of elements to delete, elements to add)\
toFixed: fix precision in decimal\
flat: returns array with individual values spread out, recursively\

## random number in range [min, max]
```Javascript
console.log(min + Math.floor( ( Math.random() * (max - min + 1) ) ) );
```

block scope: means which variables are accessible inside a block. matlab jo variables ek block mein defined hn wo uske bahar accessible nhi honge\
fn scope: which variables area accessible inside a fn. matlab jo variables fn k andar defined hnwo uske bahaar accessible nhi honge 


## closures
Nested functions. fn inside fn. inner fn can access values of outer fn but outer fn cannot access values of inner fn
```javascript
function One() {
    const username = "Aditya";
    function Two() {
        const website = "blogdekho";
        console.log(username);
    }
     console.log(website);  error: website is not defined
    Two();
}
One();
```

## Arrow fn
context: space where some code is written eg. current scope it could be inside an object, if-else. matlab values ki jo bhi variables hn wo kya hold kr rhe hn\
this: reference to current context
```javascript
// in browsers window object is present in the GEC. but in other runtimes no such global object is present
// that is why in node.js when this by default points to an empty object
const myObj = {
    username: "Aditya",
    codes: true,
    message: function() {
        console.log(`${this.username}, welcome to blog dekho`);
    }
};
myObj.message();
console.log(this);  empty object {} because global EC is empty
```

Regular fn: this is dynamic, determined by how the function is called\
Arrow fn: this is lexical, determined by the surrounding scope where the function is defined
```javascript
function getData() {
    const username = "Aditya";
    console.log(this.username);  undefined. because this is only used inside objects and not inside fn
}
getData();

const fetchData = () => {
    console.log(this);  {}. this refers to global object in case of arrow fn
}
```

## implicit return. no need to write return under ()
```javascript
const addNum = (num1, num2) => (num1 + num2)
const getObj = () => ({username: "Aditya", codes: true});
```

## IIFE
it eliminates the pollution in global scope by encapsulating variables and fn in a local scope which cannot be accessed from globally.
this prevents variables and fn from "leaking" into the global scope. No variables inside iife can interact with global scope preventing naming conflicts and unexpected behavours
```js
// always end the first iife with ; because iife don't know where to stop it's own\
// context when multiple iife declarations area there
((name) => {
    console.log('this is some code');

})('Aditya')
(() => {
    console.log('reached second iife');
})();
```


 ## Execution Context
 1. Global EC
 2. Function EC
 ### Execution context has 2 phases:
 1. memory creation phase
 2. code execution phase
<img width="600" alt="Image" src="https://github.com/user-attachments/assets/b416004c-a504-4842-86fb-16e51d927554" />

 ## points to note
 1. whenever a JS program runs a GEC is created
 2. along with it a this pointer is also created which points to the EC of its parent
 3. a new executional context creates following two things:
      a. new variable env
      b. execution thread
