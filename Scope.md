# My repository about Scope Hoisting TDZ

## Scope

### What is Scope in JavaScript ?
Scope determines the accessibility of variables, objects, and functions from different parts of the code.
+ Scope Types:
  + Global Scope 
  + Local Scope
    + Function Scope
    + Block Scope
  + Module Scope
    
```javascript

// Global Scope

function SumOfTwoNum(num1, num2){
    // Local Scope: Function Scope
    let sum =  num1 + num2;

    return sum;
}

// ❌ I can`t use Variable with keyword let or const from Local Scope in Global Scope 
console.log(sum);
```

### The role of Global Scope

+ Global Scope
  Global scope is the widest
  scope available. Variables declared in global
  scope are accessible from anywhere in your
  code, whether it's inside functions, conditional
  statements, loops, or other blocks of code.

  Outside of any function or block

  Variables declared in global scope are accessible everywhere

  ```javascript
  
  let name = "Faloniev Faloni"

  var age = 16;

  function get(){

      return `Hello! ${name} have ${age} old!`
  
  }

  ```

### The role of Local Scope

+ Local Scope:
  + Function Scope

    + Function Scope : The scope created with a function.
    Also called local Scope

    ```javascript
    
    // code here can use carName

    function myFunction() {

        carName = "Volvo";

        return `My favourite Car is ${carName}`
    }

    ```

    + Variables accessible only inside function, NOT outside

    + Function Scope

    + Function scope in JavaScript refers to the scope of variables and functions that are defined
    within a function. Variables and functions declared with the var keyword have function
    scope.

    + Variables declared inside a function are accessible only within that function and any nested
    functions. They are not accessible outside of the function in which they are defined. This
    means that variables declared within a function cannot be accessed before their
    declaration or outside of the function.



  + Block Scope
    + Block scope in JavaScript refers to the scope of variables and functions that are defined
    within a block of code, such as within a pair of curly braces {}. Variables and functions
    declared with let and const keywords have block scope.Variables declared inside a function
    are accessible only within that function and any nested functions. They are not accessible
    outside of the function in which they are defined. This means that variables declared within a
    function cannot be accessed before their declaration or outside of the function.

    ```javascript

    let cnt = 0;

    // Block Scope

    for(let i=0; i<=10; i++){
        cnt += i;
    }

    console.log(cnt);

    ```



## What is Hoisting ?

+ Hoisting is a JavaScript mechanism where variables and function declarations are moved to the
top of their scope before code execution.
  Hoisting in JavaScript is a behavior in which a function or a variable can be used before
declaration.

```javascript

    console.log(num);

    let sum = num + digit;

    var digit = 9;

    var num = 124;

```

### Function (declaration) - Hoisting



  + In JavaScript, function declarations are fully
hoisted. This means that both the function's
name and its definition are moved to the top
of their scope, making the function available
to be called anywhere in that scope, even
before its actual declaration in the code.



```javascript

console.log(fibonacciIter(10)); // 55

function fibonacciIter(n) {
    let a = 0, b = 1;
    for (let i = 2; i <= n; i++) {
        [a, b] = [b, a + b];
    }
    return n ? b : a;
}

```

## Temporal dead zone let and const 

+ TDZ : Is the term to describe the state where
variables are un-reachable. They are in
scope, but they aren't declared.
The let and const variables exist in the TDZ
from the start of their enclosing scope until
they are declared.

```javascript

console.log(myVar); // ❌ ReferenceError: Cannot access 'myVar' before initialization
let myVar = 10;
console.log(myVar); // ✅ 10


```