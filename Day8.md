# Day 8


## I Learned: 

- Thread of Execution + Memory + Call Stack
- pass functions as parameters
- Pair Programming
- Promises 
  

## Code Snippets:

Important Code: 
```JS

```

## challenges:

challenge 1:

```JS
const squareList = arr => {
  arr = arr.filter(x => x > 0);
  arr = arr.filter (x => x%1 == 0);
  arr = arr.map(x => x*x); 
  // Only change code below this line
  return arr;
  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);
```


challenge 2:

```JS
// Only change code below this line
function urlSlug(title) {
  
  title = title.split(" ");
  title = title.filter(x => x !== "");
  title = title.map(x => x.toLowerCase());
  title = title.join("-");
    
    return title;

}
// Only change code above this line
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");
```


challenge 3:

```JS
//Question 1:
function mapAsync(array, callback) {
  return new Promise((resolve, reject) => {
    const mappedArray = [];
    let completedCount = 0;

    if (array.length === 0) {
      resolve(mappedArray);
      return;
    }

    array.forEach((item, index) => {
      callback(item)
        .then((result) => {
          mappedArray[index] = result;
          completedCount++;

          if (completedCount === array.length) {
            resolve(mappedArray);
          }
        })
        .catch(reject);
    });
  });
}

//Question 2:
function sumRange(start, end) {
  if (start === end) {
    return start;
  }
  return start + sumRange(start + 1, end);
}
```





