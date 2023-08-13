# Day 5


## I Learned: 

- map & filter
- spread
  

## Code Snippets:

Important Code: 
```JS
for(let n of numbers) {
  console.log(n);
}
let three = `${1+2}`
setTimeout(() => console.log("Hello World"),1000);
```

Exercise 1: 

```JS
let firstName = "Issa";
let lastName = "Abbadi";
if (firstName.length > lastName.length) {
console.log(firstName,  "is longer than ", lastName);
}

function isEmpty(array) {
  if(array.length === 0) {
 return true;
} else {
return false;
}
}

if([]) {
  console.log("truthy");
} else {
  console.log("falsy");

}

```

Exercise 2: 

```JS
const names = spices.map(spice => spice.name);
const nicknames =  spices.filter(spice => spice.nicknames.endsWith("y"));
```

Exercise 3: 

```JS


```

Quiz part 3:
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

      for (button of optionButtons) {
        button.addEventListener("click", (event) => {
          explanation.textContent = fact.explanation;
        });
      }

      for (let button of optionButtons) {
        button.addEventListener("click", (event) => {
          explanation.textContent = fact.explanation;
        });
      }

      for (let otherButton of optionButtons) {
        disable(otherButton);
      }

      if (isCorrect(button.value)) {
        button.classList.add("correct");
      } else {
        button.classList.add("incorrect");
      }
    </script>
```

Doggos Part1:
```JS
// TODO 1
      // Given an array of possible answers, a correct answer value, and a number of choices to get,
      // return a list of that many choices, including the correct answer and others from the array
      function getMultipleChoices(n, correctAnswer, possibleChoices) {
        const choices = [];
        choices.push(correctAnswer);
        while (choices.length < n) {
          let candidate = getRandomElement(possibleChoices);
          if (!choices.includes(candidate)) {
            choices.push(candidate);
          }
        }

        return shuffleArray(choices);
      }
```

## Challenges: 

challenge 1: 

```JS
function checkSign(num) {
    return (num === 0) ? "zero"
          :(num > 0) ? "positive" 
          :"negative";
}

checkSign(10);
```



challenge 2: 

```JS
// Only change code below this line

const ratings = watchList.map((movie) => ({
  title : movie.Title,
  rating: movie.imdbRating
}))

// Only change code above this line

console.log(JSON.stringify(ratings));
```


challenge 3: 

```JS
// Only change code below this line

const filteredList = watchList.filter(movie => movie.imdbRating >= 8.0).map(movie => ({
  title: movie.Title,
  rating: movie.imdbRating
}));

// Only change code above this line

console.log(filteredList);
```



challenge 4: 

```JS
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
  // Only change code below this line
  if (strokes == 1) {
    return names[0];
  } else if (strokes <= par - 2) {
    return names[1];
  } else if (strokes === par - 1) {
    return names[2];
  } else if (strokes === par) {
    return names[3];
  } else if (strokes === par + 1) {
    return names[4];
  } else if (strokes === par + 2) {
    return names[5];
  } else {
    return names[6];
  }

  return "Change Me";
  // Only change code above this line
}

golfScore(5, 4);
```

