# Callbacks in JS

+ Hand Drawn Arrow
A callback in JavaScript is a function that is passed
to another function as an argument and is later
invoked when that function completes its
execution.
  ```javascript
  function drawArrow(color, callback) {
    callback(color);
  }

  function showColor(color) {
    return `The color is ${color}`;
  }

  drawArrow('red', showColor); // Outputs: The color is red
  ```

## Array Callbacks

### forEach()

+ The forEach method in JavaScript is used to
execute a specified function once for each
element in an array. It does not return a new
array, which distinguishes it from the map or
filter methods.
  ```javascript
  function printArray(arr) {
    return arr.forEach(elem)=> console.log(elem);
  }

  printArray([1, 2, 3, 4, 5]); // Outputs: 1, 2, 3, 4, 5
  ```

### map()
+ The map method in JavaScript creates (returns) a new array by applying a function
to each element of the original array. This is especially useful when you need to
transform an array into another
  ```javascript
  function typeArray(arr) {
    return arr.map(elem=> typeof elem);
  }
  typeArray([1, 2, 3, 4, 5]); // Outputs: [number, number, number, number, number]
  ```
### filter()
+ The filter method in JavaScript creates (returns) a new array containing elements
that satisfy a certain condition. If the condition returns false, the element is
excluded. This is useful for filtering data.
  ```javascript
  function filterArray(arr) {
    return arr.filter(elem=> elem % 2 === 0);
  }
  filterArray([1,2,3,4,5])
  ```

### find()
+ The find method is used to find the first element in an array that satisfies a given
condition. It returns the first matching element, or undefined if no element matches
the condition.
  ```javascript
  function findArray(arr) {
    return arr.find(elem=> elem == 2);
  }
  findArray([1,2,3,4,5]) // Outputs: 2
  ```

### toSorted()
+ The toSorted method in JavaScript is a new method added in recent versions of the
language. It is similar to the sort method, but with an important difference: toSorted
does not modify the original array, but returns a sorted copy of it. This makes it safe
to use when you want to preserve the original data.
  ```javascript
  function sortArray(arr) {
    return arr.toSorted((a, b) => a - b);
  }
  sortArray([5, 3, 8, 1, 2]) // Outputs: [1, 2, 3, 5, 8]
  ```

### reduce()
+ The reduce method in JavaScript is used to process each element of an array
sequentially to calculate a single value (such as a sum, product, or object). It takes a
callback function and an initial value.
   + callback: A function to call for each element. It takes:
     + accumulator: The accumulated value.
     + currentValue: The current element of the array.
     + index (optional): The index of the current element.
     + array (optional): The original array.
   + initialValue: The initial value for the accumulator.
   ```javascript
   function sumArray(arr) {
    return arr.reduce((accumulator, currentValue) => accumulator + currentValue, 0); 
   }
   sumArray([1, 2, 3, 4, 5]) // Outputs: 15
+ Notes:
If initialValue is not specified, the first value of accumulator becomes
the first element of the array, and currentValue becomes the second.
It is better to always specify initialValue for greater predictability.

