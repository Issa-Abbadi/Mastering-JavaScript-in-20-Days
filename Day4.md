# Day 4


## I Learned: 

- Arrow functions
- return undefined is the default return
- let and var scopes
- event listeners
  

## Code Snippets:

Important Code: 
```JS
const mul = x => x*x
documnet.addEventListener("click", () => {
console.log("Clicked");
}
```

Exercise 1: 

```JS
function multiply(a,b) {
  return a * b;
}

const yell = function (saying) {
return saying.toUpperCase();
}

function longerThan(a1, a2){
  return a1.length > a2.length;
}

```

Exercise 2: 

```JS
const divide = (x,y) => x/y;

const whisper = (text) => {
const lc =text.toLowerCase();
console.log(lc);
return lc;
}

const shorterThan = (a1, a2) => a1.length < a2.length;
```

Exercise 3: 

```JS
let trueButton = optionButtons[0];

trueButton.addEventListener("click", (event) => {
  trueButton.textContent = trueButton.textContent.toUpperCase();
});

let h1 = documnet.getElementByTagName("h1");
h1 = h1[0];

h1.addEventListener("mouseover", () => {
  h1.textContent = "hovering";
});

h1.addEventListener("mouseout", () => {
  h1.textContent = "Quiz.js";
});


```

Quiz part 2:
```JS
    <script type="text/javascript">
      const statement = document.getElementById("statement");
      const optionButtons = document.querySelector("#options").children;
      const explanation = document.getElementById("explaination");

      const fact = {
        statement: "Arrays are like objects",
        answer: true,
        explanation: "Arrays are a kind of object with special properties",
      };

      statement.textContent = fact.statement;

      const disable = (button) => {
        button.setAttribute("disabled", "");
      };

      const enable = (button) => {
        button.removeAttribute("disabled");
      };

      const isCorrect = (guessString) => {
        return guessString === fact.answer.toString();
      };
</script>
```

## Challenges: 

challenge 1: 

```JS
// Declare the myGlobal variable below this line
let myGlobal = 10;

function fun1() {
  oopsGlobal = 5;

}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```



challenge 2: 

```JS
function myLocalScope() {
  // Only change code below this line
  let myVar;
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```


challenge 3: 

```JS
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  let outerWear = "sweater";
  return outerWear;
}

myOutfit();
```


challenge 4: 
function nextInLine(arr, item) {
  arr[arr.length] = item
  const r = arr[0];
  for(let i=1; i<arr.length ; i++){
      arr[i-1] = arr[i];
  }
  return r;
  
  return item;
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```JS
 
```
