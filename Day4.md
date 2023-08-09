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

```



challenge 2: 

```JS

```


challenge 3: 

```JS

```


challenge 4: 

```JS
 
```
