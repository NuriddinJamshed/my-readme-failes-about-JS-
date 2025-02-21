# Array in JS

## What is a array in JavaScript?

+ An array is an object that holds values (of any type) not particularly in named
properties/keys, but rather in numerically indexed positions.

+ In JavaScript, an array is an ordered list of values. Each value is called an element
specified by an index.First, an array can hold values of mixed types.

+ An array is a special variable, which can hold more than one value:
  ```javascript
  // Simple array in Js
  let arr = [0, 1, 2, 3, 4, 5];
  ```
  + Here, `arr` is the name of the array and `[0, 1, 2, 3, 4, 5]` are the elements stored in the array.
  + Array elements are accessed using their index, starting from 0.
  + Array has properties like length, which gives the number of elements in the array.

### Change elements in array.

+ You can also add elements or change the elements by accessing the index value. Suppose
an array has two elements. If you try to add an element at index 3 (fourth element), the
third element will be undefined.
  ```javascript
  // Changing element
  let arr = [0, 1, 2, 3, 4, 5]

  arr[3] = 6; // Change the 4th element to 6

  console.log(arr) // Output: [0, 1, 2, 6, 4, 5]
  ```
  + Accessing elements of an array using index

  ```javascript
  // Adding element
  let arr = [0, 1, 2, 3]

  arr[4] = 4; // Add 4 at the 5th index

  console.log(arr) // Output: [0, 1, 2, 3, 4]
  ```
## Array methods

  + pop() - Removes the last element from an array and returns that element.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.pop(); // Removes 5 from the array
    ```
  + push() - Adds one or more elements to the end of an array and returns the new length of the array.
    ```javascript
    let arr = [0, 1, 2, 3];
    arr.push(4, 5); // Adds 4 and 5 to the array
    ```
  + shift() - Removes the first element from an array and returns that element.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.shift(); // Removes 0 from the array
    ```
  + unshift() - Adds one or more elements to the beginning of an array and returns the new
    ```javascript
    let arr = [0, 1, 2, 3];
    arr.unshift(4, 5); // Adds 4 and 5 at the beginning of the array
    ```
  + concat() - Merges two or more arrays and returns a new array.
    ```javascript
    let arr1 = [0, 1, 2];
    let arr2 = [3, 4, 5];
    arr1.concat(arr2); // Merges arr1 and arr2 and returns [0, 1, 2, 3, 4, 5]
    ```
  + slice() - Extracts a section of an array and returns a new array.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.slice(1, 4); // Returns [1, 2, 3]
    ```
  + splice() - Removes elements from an array and, if necessary, inserts new elements in their
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.splice(1, 2, 'a', 'b'); // Removes 1 and 2 from the array and inserts 'a' and 'b'
    ```
  + indexOf() - Returns the first index at which a given element can be found in the array
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.indexOf(3); // Returns 3
    ```
  + includes() - Returns true if an element exists in the array, otherwise false.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.includes(3); // Returns true
    ```
  + toString() - Returns a string representation of an array.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.toString(); // Returns "0,1,2,3,4,5"
    ```
  + join() - Joins all elements of an array into a string, separated by commas or
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.join('-'); // Returns "0-1-2-3-4-5"
    ```
  + toReversed() - Returns a new array with the elements in reverse order.
    ```javascript
    let arr = [0, 1, 2, 3, 4, 5];
    arr.reverse(); // Returns [5, 4, 3, 2, 1, 0]
    ```