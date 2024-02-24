### Call and Apply



  - Both `.call` and `.apply are used to invoke functions and the first parameter will be used as the value of this within the function.
 -  However, `.call` takes in comma-separated arguments as the next arguments while `.apply` takes in an array of arguments as the next argument.
 -  An easy way to remember this is C for `call` and comma-separated and A for `apply` and an array of arguments.



```javascript

function add(a, b) {
  return a + b;
}

console.log(add.call(null, 1, 2)); // 3
console.log(add.apply(null, [1, 2])); // 3
```
