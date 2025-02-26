# Object Methods

## Object.keys()

### Object keys() method returns an array of a given object's own enumerable property names, in the same order as that provided by a for...in loop.

```javascript

let obj = { 
            name: 'John',
            age: 30,
            city: 'New York', 
          };

console.log(Object.keys(obj)); // Output: ["name", "age", "city"]
```

## Object.values()
### Object.values() method returns an array of a given object's own enumerable property values, in the same order as that provided by a for...in loop.

```javascript

let obj = { 
            name: 'John',
            age: 30,
            city: 'New York', 
          }

console.log(Object.values(obj)); // Output: ["John", 30, "New York"]

```

## Object.entries()
### Object.entries() method returns an array of a given object's own enumerable property [key, value] pairs, in the same order as that provided by a for...in loop.

```javascript

let obj = {
    name: 'John',
    age: 30,
    city: 'New York',
}

console.log(Object.entries(obj)); // Output: [["name", "John"], ["age", 30], ["city", "New York"]]
```

## Object Mechanisms
+ Object mechanisms are used to manipulate and access the properties of objects in JavaScript. They provide built-in methods and functionalities that make working with objects more efficient and intuitive.
+ We have two main types of object mechanisms:
  + Destructuring: 
    + This is a feature that allows us to extract values from objects and assign them to variables in a more concise and readable way.
      ```javascript
      let obj = { 
          name: 'John',
          age: 30 
       };
  
       let { name, age } = obj;
  
       console.log(name); // Output: John
       console.log(age); // Output: 30
       ```
  + Spread:
    + This is a feature that allows us to copy the properties of one object to another object.
      ```javascript
      let obj1 = { 
        name: 'John',
        age: 30 
      }

      let obj2 = {...obj1 }; // obj2 now has the same properties as obj1
      console.log(obj2.name); // Output: John
      ```

## Keyword "this"

+ The "this" keyword refers to the current object in which the function is being executed.
+ General rules for using "this" keyword:
  + In Object methods, "this" refers to the object itself.
    ```javascript
    let obj = {
        name: 'John',
        age: 30,
        about(){
            return `My name is ${this.name} and I am ${this.age} years old.`;
        }
    }

    console.log(obj.about()); // Output: My name is John and I am 30 years old.
    ```
  + In arrow functions, "this" behaves similarly to how it behaves in regular functions.
    ```javascript
    let obj = {
        name: 'John',
        age: 30,
        about: () => this.name
    }

    console.log(obj.about()); // undefined
    ```
  + Inside the functions defined within other functions, "this" refers to the global object (window in a browser environment).
    ```javascript
    function outerFunction(){
        return this.name;
    }

    console.log(outerFunction()); // Output: undefined
    ```

