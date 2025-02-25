### Object in JS

## What is Object❓

+ Object is a collection of properties and methods. 
+ Objects are created using curly braces { }.
+ Objects has :
  + key
  + value
  ```javascript

  let car = {
      // Key: Value pair
      name: 'Tesla',
      model: 'Model S',
      year: 2020,
  }

  console.log(car); // Output: { name: 'Tesla', model: 'Model S', year: 2020 }
  ```
  + We can access the properties of an object using dot notation or bracket notation.  


    ```javascript
    let person = {
      name: "John";
      lastName: "Doe";
    }
    //using dot notation
    console.log(person.name); // Output: John
    ```
  + We can also access the properties using bracket notation.

  
    ```javascript
    let phone = {
        name: "iPhone",
        model: "15 pro",
    }
    // Using bracket notation
    console.log(phone[name])
    ```
