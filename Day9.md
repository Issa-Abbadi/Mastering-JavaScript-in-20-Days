# Day 9


## I Learned: 

- Closuers
- Web features
- introduction to Async functions
  

## Code Snippets:

Important Code: 
```JS

```

## challenges:

challenge 1:

```JS
function createCounter(start) {
  let count = start;

  return function() {
    count++;
    return count;
  };
}

```


challenge 2:

```JS
function calculateAverage(nums) {
  return function() {
    const sum = nums.reduce((total, num) => total + num, 0);
    return sum / nums.length;
  };
}
```



challenge 3:

```JS
function powerOf(base) {
  return function(exp) {
    return Math.pow(base, exp);
  };
}
```




challenge 4:

```JS
function compose(...funcs) {
  return function(x) {
    return funcs.reduceRight((result, func) => func(result), x);
  };
}
```
