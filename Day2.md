# Day 2


## I Learned: 

- typeof shows the type of an object
- typeof null is undefined is a mistake
- === -> strict
- == -> loosey-goosy
- let vs const vs var
- statements vs expressions
  

## Code Snippets:

Important Code: 
```JS
"HelloWorld".length
"HelloWorld".indexOf("H")
"HelloWorld".indexOf("Hello")
"HelloWorld".includes("H")
"HelloWorld".startsWith("Hello")

```

Exercise 1: 

```JS
document.getElementById("pl-name).append(" Vakil")
document.title.indexOf("T")
document.title.includes("JavaScript")
document.querySelector("header h1).textContent = document.querySelector("header h1).textContent.toUpperCase();

```

Exercise 2: 

```JS
1 + 2
8 * 7 / 7
(24 - 8) * 1  * 7
```

Exercise 3: 

```JS
const issa = "Issa";
let combinedParentAge = 23 + 24;
let board = document.querySelector("#board");
board.childern.length
```

## Challenges: 

challenge 1: 

```JS
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b); // ture because "==" only compares the values not the types
console.log(b === c); // false because "===" compares values and types which don't match
console.log(!!d); // true because the String "false" is considered true in boolean and "!!d" is the same as "d"
```



challenge 2: 

```JS
console.log(4 + 5 * "7"); // output is 39
// because first "7" is converted to number 7 then
// 5 * 7 is evaluated
// then 4 + 35 is evaluated

```


challenge 3: 

```JS
let result = 5 + 2 * 3 - 1; // result = 10
// because it will evaluate depending on the priority of the operations
// first multiply 2 * 3 = 6
// then evaluate 5 + 6 -1 from left to right which is 10

```


challenge 4: 

```JS

let x = 10;
let y = '10';
console.log(x == y); // true because "==" only compares the values not the types
console.log(x === y); // false because "===" compares values and types which don't match

```

challenge 5: 

```JS
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result); // output true
// steps
// evaluate 15 > 10 which is true
// evaluate true && true which is true because isPositive is true
// 15 < 0 is false
// true || false is true 

```
