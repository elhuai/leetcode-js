# [Easy] LeetCode JS 30 - 2635. Apply Transform Over Each Element in Array

## LeetCode 30 Days of JavaScript

### 2635. Apply Transform Over Each Element in Array

## Description:

Given an integer array arr and a mapping function fn, return a new array with a transformation applied to each element.

The returned array should be created such that returnedArray[i] = fn(arr[i], i).

Please solve it without the built-in Array.map method.



### Example 1:

Input: arr = [1,2,3], fn = function plusone(n) { return n + 1; }
Output: [2,3,4]
Explanation:
const newArray = map(arr, plusone); // [2,3,4]
The function increases each value in the array by one. 

### Example 2:
Input: arr = [1,2,3], fn = function plusI(n, i) { return n + i; }
Output: [1,3,5]
Explanation: The function increases each value by the index it resides in.

## Answer:

```javascript
var map = function(arr, fn) {
    let answer = []
    for (let i = 0; i < arr.length; i++) {
        let value = fn(arr[i],i)
        answer.push(value)
    }
    return answer
};
```
