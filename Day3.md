# Day 3


## I Learned: 

- .pop() to get from array .push("Hello") to add to the array
- "lonely" == ["lonely"] -> true
- important methods for arrays .sort() .join(" & ") .concat([4,5,6])
- mutable vs immutable (.freeze() ->  to make it immutable)
- console.error() console.warn()
  

## Code Snippets:

Important Code: 
```JS
["lions","tigers"].join(" & ");
[1,2,3].concat([4,5,6]);


```

Exercise 1: 

```JS
const issa = {
name: "issa",
home: "yabad",
languages: ['Arabic','English'],
pet: null,
age: 23
}

```

Exercise 2: 

```JS

```

Exercise 3: 

```JS
spiceGirls.motto
spiceGirls.members[1]
spiceGirls.albums[1]
spiceGirls.members[4].name
```

Quiz part 1:
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
```

## Challenges: 

challenge 1: 

```JS
function forecast(arr) {
  // Only change code below this line

  return arr.slice(2,4);
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```



challenge 2: 

```JS
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment, 'is' , 'fun'];
  return sentence;
}

console.log(spreadOut());
```


challenge 3: 

```JS
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  for(let i=0; i < contacts.length ; i++){
        if(name === contacts[i].firstName){
          for (var key in contacts[i]) {
            if (key === prop) {
          return contacts[i][prop];
        } 
          
        
          }
          return "No such property";
  }
  }
  return "No such contact";
}

lookUpProfile("Akira", "likes");

```


challenge 4: 

```JS
 function reusableFunction() {
   console.log("Hi World");
 }

 reusableFunction();
```

challenge 5: 

```JS
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}

function addFive() {
  sum += 5;
}



addThree();
addFive();
```


challenge 6: 

```JS
function timesFive(num) {
  return num * 5;
}
```
