## Flatten the nested array

- Create a function flattenArray that accepts an array arr.
- Inside the function, declare an empty array result.
- Iterate over each element in arr using a loop (e.g., forEach).
- Check if the current element is an array with Array.isArray(element).
- If not an array, use result.push(element) to add the element to result.
- If it is an array, call flattenArray recursively with this element and concatenate the result to result using result = result.concat(flattenArray(element)).
- After the loop, return result, which now contains the flattened array.

```js
function flattenArrays(arr){

  let result =[];
  arr.forEach(element => {
    if(Array.isArray(element)){
      // Recursive Case: If the item is an array, call flattenArray recursively
      result = result.concat(flattenArrays(element));
    }else{
      // Base Case: If the item is not an array, add it to the result array directly
      result.push(element);
    }
    
  });
  return result;

}

console.log(flattenArrays([1, [2, [3, [4, 5]]], 6]));
```
