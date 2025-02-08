# [Easy] LeetCode JS 30 - 2621. Sleep

## LeetCode 30 Days of JavaScript

### 2621. Sleep

## Description:

Given a positive integer millis, write an asynchronous function that sleeps for millis milliseconds. It can resolve any value.

### Example 1:

Input: millis = 100
Output: 100
Explanation: It should return a promise that resolves after 100ms.
let t = Date.now();
sleep(100).then(() => {
console.log(Date.now() - t); // 100
});

### Example 2:

Input: millis = 200
Output: 200
Explanation: It should return a promise that resolves after 200ms.

## Answer:

```javascript
async function sleep(millis) {
  return new Promise((resolve, reject) => {
    setTimeout(resolve, millis);
  });
}
```
