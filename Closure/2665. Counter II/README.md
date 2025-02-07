# [Easy] LeetCode JS 30 -2665. Counter II

## LeetCode 30 Days of JavaScript

### 2665. Counter II

## Description:

Write a function createCounter. It should accept an initial integer init. It should return an object with three functions.

The three functions are:

increment() increases the current value by 1 and then returns it.
decrement() reduces the current value by 1 and then returns it.
reset() sets the current value to init and then returns it.

### Example 1:
Input: init = 5, calls = ["increment","reset","decrement"]
Output: [6,5,4]
Explanation:
const counter = createCounter(5);
counter.increment(); // 6
counter.reset(); // 5
counter.decrement(); // 4

## Answer:

```javascript
var createCounter = function(init) {
    let resetNum = init
    let tempNum = init
    return{
        increment(){
            tempNum =tempNum + 1
            return tempNum
        },
        decrement(){
            tempNum -= 1
            return tempNum
        },
        reset(){
            tempNum = resetNum
            return tempNum
        }
    }
};
```
