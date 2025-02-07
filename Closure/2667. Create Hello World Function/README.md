# [Easy] LeetCode JS 30 - 2667. Create Hello World Function (創建閉包函式)

## LeetCode 30 Days of JavaScript

### 2667. Create Hello World Function (創建閉包函式)

## Description:

Write a function `createHelloWorld`. It should return a new function that always returns "Hello World".

### Example 1:

**Input:** `args = []`  
**Output:** `"Hello World"`  
**Explanation:**

```javascript
const f = createHelloWorld();
f(); // "Hello World"
```

Any arguments could be passed to the function but it should still always return "Hello World".

## Answer:

```javascript
var createHelloWorld = function () {
  return function () {
    return "Hello World";
  };
};
```
