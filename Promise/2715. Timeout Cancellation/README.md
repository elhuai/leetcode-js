# [Easy] LeetCode JS 30 - 2715. Timeout Cancellation

## LeetCode 30 Days of JavaScript

### 2715. Timeout Cancellation

## Description:

Given a function fn, an array of arguments args, and a timeout t in milliseconds, return a cancel function cancelFn.

After a delay of cancelTimeMs, the returned cancel function cancelFn will be invoked.

setTimeout(cancelFn, cancelTimeMs)
Initially, the execution of the function fn should be delayed by t milliseconds.

If, before the delay of t milliseconds, the function cancelFn is invoked, it should cancel the delayed execution of fn. Otherwise, if cancelFn is not invoked within the specified delay t, fn should be executed with the provided args as arguments.

### Example 1:

Input: fn = (x) => x \* 5, args = [2], t = 20
Output: [{"time": 20, "returned": 10}]

Explanation:
const cancelTimeMs = 50;
const cancelFn = cancellable((x) => x \* 5, [2], 20);
setTimeout(cancelFn, cancelTimeMs);

The cancellation was scheduled to occur after a delay of cancelTimeMs (50ms), which happened after the execution of fn(2) at 20ms.

### Example 2:

Input: fn = (x) => x\*\*2, args = [2], t = 100
Output: []

Explanation:
const cancelTimeMs = 50;
const cancelFn = cancellable((x) => x\*\*2, [2], 100);
setTimeout(cancelFn, cancelTimeMs);

The cancellation was scheduled to occur after a delay of cancelTimeMs (50ms), which happened before the execution of fn(2) at 100ms, resulting in fn(2) never being called.

## Answer:

```javascript
var cancellable = function (fn, args, t) {
  const timer = setTimeout(() => fn(...args), t);

  return () => clearTimeout(timer);
};
```
