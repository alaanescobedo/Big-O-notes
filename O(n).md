### **O(n) -- Linear time**

O(n) is a notation for the number of operations needed to complete a task. 
It is used to indicate that the time complexity of a function is **linear**.

By linear, we mean that the time complexity of a function is directly proportional to the size of the input.

The algorithm will going through the list of items in the list once, one by one.
``` javascript
const arrayOf10 = new Array(10).fill(0).map((_, i) => i + 1)
const arrayOf100 = new Array(100).fill(0).map((_, i) => i + 1)
const arrayOf1000 = new Array(1000).fill(0).map((_, i) => i + 1)


const myOperation = (array) => {
  array.forEach(element => { // O(n)
    console.log(element) // O(1)
  });
}

myOperation(arrayOf10) // O(n) => Linear Time Complexity == O(10) => Will require 10 operations to complete the task
myOperation(arrayOf100) // O(n) => Linear Time Complexity == O(100) => Will require 100 operations to complete the task
myOperation(arrayOf1000) // O(n) => Linear Time Complexity == O(1000) => Will require 1000 operations to complete the task
```
