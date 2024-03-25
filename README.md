# JavaScript Interview Questions

Welcome to our JavaScript interview questions repository! Here, you'll find a collection of common JavaScript interview questions along with their answers and examples.

## Question 1: What is a closure in JavaScript?

### Answer:

A closure is a function bundled together with its lexical environment (the scope chain) at the time of its creation. It allows the function to retain access to variables from its containing scope even after that scope has finished executing.

### Example:
```javascript
function outerFunction() {
  let outerVariable = "I am from the outer function";

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

const closureExample = outerFunction();
closureExample(); // Output: I am from the outer function 
```

## Question 2: Explain the difference between var, let, and const in JavaScript.?

### Answer:

var:
Function-scoped (declared within a function, accessible within that function and any nested functions).
Can be redeclared and reassigned within the same scope, leading to potential scoping issues.
let:
Block-scoped (declared within a block of code using curly braces {}, accessible only within that block).
Cannot be redeclared within the same scope, prevents accidental overwrites.
Can be reassigned within the same block.
const:
Block-scoped, similar to let.
Cannot be redeclared or reassigned after initialization, ensures data integrity.

### Example:
```javascript
function example() {
  var x = 10; // Function-scoped, accessible within the function
  if (true) {
    let y = 20; // Block-scoped, accessible only within this block
    const z = 30; // Block-scoped, cannot be reassigned or redeclared
  }

  console.log(x); // Accessible: 10
  // console.log(y); // ReferenceError: y is not defined (outside its block)
  console.log(z); // Accessible: 30
}

example();
```




