# [Easy] LeetCode JS 30 - 2619. Array Prototype Last

## LeetCode 30 Days of JavaScript

### 2619. Array Prototype Last

## Description:

Given an array arr and a chunk size size, return a chunked array.
Write code that enhances all arrays such that you can call the array.last() method on any array and it will return the last element. If there are no elements in the array, it should return -1.

You may assume the array is the output of JSON.parse.

### Example 1:

Input: nums = [null, {}, 3]
Output: 3
Explanation: Calling nums.last() should return the last element: 3.

### Example 2:

Input: nums = []
Output: -1
Explanation: Because there are no elements, return -1.

## Answer:

```javascript
Array.prototype.last = function () {
  return this.length ? this[this.length - 1] : -1;
};
```
