# [Easy] LeetCode JS 30 -2620. Counter

## LeetCode 30 Days of JavaScript

### 2620. Counter

## Description:

Given an integer n, return a counter function. This counter function initially returns n and then returns 1 more than the previous value every subsequent time it is called (n, n + 1, n + 2, etc).

### Example :

Input:
n = 10
["call","call","call"]
Output: [10,11,12]
**Explanation:**

```javascript
counter() = 10 // The first time counter() is called, it returns n.
counter() = 11 // Returns 1 more than the previous time.
counter() = 12 // Returns 1 more than the previous time.
```

Any arguments could be passed to the function but it should still always return "Hello World".

## Answer:

```javascript
const createCounter = (n) => {
  let answer = n - 1;

  return () => {
    answer++;
    return answer;
  };
};
```
