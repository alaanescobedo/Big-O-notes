### **O(n^2) -- Quadratic**

This notation is characterized by having a complexity proportional to the square of our input.

It has a high cost and is not recommended for large data, we can commonly find it in `cycles` such as `for` with nested iterations, where each element of our input must be compared with other item.

``` javascript
const arrayOf10 = new Array(10).fill(0).map((_, i) => i + 1)
const arrayOf100 = new Array(100).fill(0).map((_, i) => i + 1)
const arrayOf1000 = new Array(1000).fill(0).map((_, i) => i + 1)


const myOperation = (array) => { // O(n^2)
  array.forEach(element1 => { // O(n)
    array.forEach(element2 => { // O(n)
      console.log([element1, element2]) // O(1)
    });
  });
}

myOperation(arrayOf10) // O(n^2) => Quadratic Time Complexity == O(10^2) => Will require 100 operations to complete the task
myOperation(arrayOf100) // O(n^2) => Quadratic Time Complexity == O(100^2) => Will require 10000 operations to complete the task
myOperation(arrayOf1000) // O(n^2) => Quadratic Time Complexity == O(1000^2) => Will require 1000000 operations to complete the task... don't try it at home.
```