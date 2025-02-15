# String in JS

## How to create a string?

We have 3 way to create a string:
  + "Double quotes"
  + 'Single quotes'
  + `Backticks``

  ```javascript

    // Double quotes
    let name = "Ivan"

    // Single quotes
    let lastname = "Ivanov"

    // Backticks
    let surname = "Ivanovich"

  ```

## What is a Method in JavaScript?

+ A method is a block of code which only runs when it is called. You can pass data, known as
parameters, into a method. Methods are used to perform certain actions, and they are also
known as functions.

### What is string Method:

+ CharAt()
  + The charAt() method returns the character at a
specified index (position) in a string. The index of the
first character is 0, the second 1, ... The index of the last
character is string length - 1 .
  ```javascript
    let text = "Hello"
    console.log(text.charAt(0))
  ```

+ At()
    + The at() method takes an integer value and returns a
new String. This method allows for positive and
negative integers. Negative integers count back from
the last string character. 
  ```javascript
  let text = "Hello"
  console.log(text.at(-1))
  ```
+ toString()
  + The toString() method returns a string representing
the object. By default toString() takes no
parameters. 
  ```javascript
    let num = 99;
    let tostr = num.toString();
  ```
+ concat()
  + The concat() method joins two or more strings. The
concat() method returns a new string. The concat()
method does not change the original string.
  ```javascript
  let text = "Hello"
  let text1 = "Suhrob"
  console.log(text.concat(" ", text1))
  ```
+ trim()
  + The trim() method removes whitespaces from both
side of sentences. The trim() method does not
change the original string.
  ```javascript
    let text = "    Hello   "
    console.log(text.trim())
  ```
+ include()
  + The includes() method returns true if a string contains
a specified string. Otherwise it returns false. The
includes() method is case sensitive.
  ```javascript
  let text = "Hello I`am Faloni and I have 12 years old!!"
  console.log(text.includes("Faloni"))
  ``` 
+ indexOf(), lastindexOf()
+ replace(), replaceAll()
+ substring(), slice()
+ split()
  + The split() method splits a string into an array of substrings. The split() method
returns the new array. The split() method does not change the original string. If (" ") is
used as separator, the string is split between words.
  ```javascript
  let text = "Hello world!!!"
  let toArr = text.split(" ");
  console.log(toArr)
  ```
+ toLowerCase(), toUpperCase()