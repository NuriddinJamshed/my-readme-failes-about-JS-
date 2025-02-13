# Recursion && CLosure

## Recursion ⁉

### What is recursion❓

+ Recursion in programming is like ❤ a
function that keeps calling itself. When a
function does this, its called a
recursively defined function. But there is a rule it has to follow: it must
have a way to stop calling itslef, or it will go on forever. This stopping rule
is called the base case

  ```javascript

  function sumTo(n) {
      return n + sumTo(n - 1); // ❌
  }

  function sumTo(num) {
      if(n== 0) {
          return 0;
      }
      return n + sumTo(n - 1); // ✅
  }

  ```

+ A recursive function function must have a condition to stop calling itself. Otherwise function is
called indefinetelly. Once the condition is met, the function stops calling itself. This called the base condition

+ First, you need a base condition num === 0.
You also need the recursive call
findFactorial(num - 1) to ensure the number
keeps reducing at each call when you pass a
new parameter of n-1.
Then you multiply the result with the previous
number num * findFactorial(num - 1) until the
base condition is met.

  ```javascript

  function findFactorial(num) {
      if(num === 0) {
          return 1;
      }
      return num * findFactorial(num - 1);
  }

  ```

