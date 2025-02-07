## Conditions


+ Condition if - else

The if-else statement is used to execute both the true part and the false part of a
given condition. If the condition is true, the if block code is executed and if the
condition is false, the else block code is executed

### Example:
```javascript
let x = 10;

if (x > 5) {
  console.log("x is greater than 5");
} else if (x === 5) {
  console.log("x is equal to 5");
} else {
  console.log("x is less than 5");
}

```

+ Condition Ternary Operator

An alternative to the if/else statement, the ternary operator allows JavaScript
developers to write concise conditional statements. It is written as “?:” and takes
three operands; a logical condition, a value to return if true, and a value to return if
false.

```javascript

function EvenOrOdd(num){

    return num % 2 == 0 ? "Even" : "Odd"

}

console.log(EvenOrOdd(21))

```

+ Condition Switch case

The switch statement evaluates an expression, matching the expression's value
against a series of case clauses, and executes statements after the first case clause
with a matching value, until a break statement is encountered. The default clause of
a switch statement will be jumped to if no case matches the expression's value

```javascript

let trueTest = 15;

switch (10+5){
    case trueTest:
        console.log("10+5 is 15");
        break;
    case 20:
        consol.log("10+5 is not 20!")
    default:
        console.log("You are not in this level!!!");
        break
}
```

## Loop

+ Loop for

The for loop in JavaScript is a control flow statement used to repeat a block of code multiple times. It is one of the most commonly used loops for iteration.

```javascript

for (let i = 1; i <= 5; i++) {
  console.log(i);
}

```

+ Loop while

The while statement creates a loop that executes a specified statement as long as
the test condition evaluates to true. The condition is evaluated before executing the
statement. The following while loop iterates as long as n is less than three. 

```javascript

let n = 0;
let x = 0;

while(n<3){
    n++;
    x += n;
}

console.log(n)

```

+ Loop do-while

The do...while statement creates a loop that executes a specified
statement until the test condition evaluates to false. 

```javascript

let res = "";
let i = 0;

do{
    i++;
    res += i;
} while (i < 5);

console.log(res);

```

## Funcitons

+ We have 3 types of FUNCTIONS in JS
  + Function Declaration
  + Function eXPRESSION
    + Anonymous
    + Arrow
  + Immediately Invoked
Function Expression
(IIFE)


+ Function Declaration

The function declaration defines a function
with the specified parameters. A function is
declared using the function keyword. The
basic rules of naming a function are similar to
naming a variable. 

It is better to write a descriptive name for your
function. For example, if a function is used to
add two numbers, you could name the
function add or addNumbers.

```javascript
function addUp(num){
    let res = 0;
    for(let i=1; i<=num; i++){
        res += i;
    }
    return res;
}

console.log(addUp(4));

```

+ Function eXPRESSION
  + Anonymus
    ```javascript
    let sumOfTwoNum = (num1, num2){
        return num1+num2;
    } 

    console.log(sumOfTwoNum(3, 4));

    ```

  + Arrow
    ```javascript
    let fibonacci = (num) => {
        let arr = [0, 1];
        for(let i = 2; i < num; i++){
            arr.push(arr[i-1]+arr[i-2]);
        }
        return arr;
    }

    console.log(fibonacci(10));
    ```

+ Immediately Invoked
Function Expression
(IIFE)

  An IIFE (Immediately Invoked Function
  Expression) is a function that runs the
  moment it is invoked or called in the
  JavaScript event loop. 

  Having a function that behaves that way
  can be useful in certain situations. IIFEs
  prevent pollution of the global JS scope

  ```javascript

  console.log((function(num1, num2){
        return num1+num2;
  })(4, 5));