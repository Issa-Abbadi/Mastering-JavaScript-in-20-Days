# Day 6


## I Learned: 

- promise (pending / fulfilled / rejected)
- await
- .then()
- async
  
  

## Code Snippets:

Important Code: 
```JS

```

Exercise 1: 

```JS


```

Exercise 2: 

```JS

```

Exercise 3: 

```JS


```



Doggos Part2:
```JS
      // TODO 2
      // Given a URL such as "https://images.dog.ceo/breeds/poodle-standard/n02113799_2280.jpg"
      // return the breed name string as formatted in the breed list, e.g. "standard poodle"
      function getBreedFromURL(url) {
        // The string method .split(char) may come in handy
        // Try to use destructuring as much as you can
        let unsplitBreed = url.split("/")[4];
        let [breed, subbreed] = unsplitBreed.split("-");
        return [subbreed, breed].join(" ").trim();
      }
      // TODO 3
      // Given a URL, fetch the resource at that URL,
      // then parse the response as a JSON object,
      // finally return the "message" property of its body
      async function fetchMessage(url) {
        const responce = await fetch(url);
        const body = await responce.json();
        const { message } = body;
        return message;
      }

      // Function to add the multiple-choice buttons to the page
      function renderButtons(choicesArray, correctAnswer) {
        // Event handler function to compare the clicked button's value to correctAnswer
        // and add "correct"/"incorrect" classes to the buttons as appropriate
        function buttonHandler(e) {
          if (e.target.value === correctAnswer) {
            e.target.classList.add("correct");
          } else {
            e.target.classList.add("incorrect");
            document
              .querySelector(`button[value="${correctAnswer}"]`)
              .classList.add("correct");
          }
        }

        const options = document.getElementById("options"); // Container for the multiple-choice buttons

        // TODO 4
        // For each of the choices in choicesArray,
        // Create a button element whose name, value, and textContent properties are the value of that choice,
        // attach a "click" event listener with the buttonHandler function,
        // and append the button as a child of the options element

        for (let choice of choicesArray) {
          const button = document.createElement("button");
          button.textContent = choice;
          button.value = choice;
          button.name = choice;
          button.addEventListener("click", buttonHandler);
          options.appendChild(button);
        }
      }

      // Function to add the quiz content to the page
      function renderQuiz(imgUrl, correctAnswer, choices) {
        const image = document.createElement("img");
        image.setAttribute("src", imgUrl);
        const frame = document.getElementById("image-frame");

        image.addEventListener("load", () => {
          // Wait until the image has finished loading before trying to add elements to the page
          frame.replaceChildren(image);
          renderButtons(choices, correctAnswer);
        });
      }

      // Function to load the data needed to display the quiz
      async function loadQuizData() {
        document.getElementById("image-frame").textContent =
          "Fetching doggo...";

        const doggoImgUrl = await fetchMessage(RANDOM_IMG_ENDPOINT);
        const correctBreed = getBreedFromURL(doggoImgUrl);
        const breedChoices = getMultipleChoices(3, correctBreed, BREEDS);

        return [doggoImgUrl, correctBreed, breedChoices];
      }

      // TODO 5
      // Asynchronously call the loadQuizData() function,
      // Then call renderQuiz() with the returned imageUrl, correctAnswer, and choices
      const [imgUrl, correctAnswer, choices] = await loadQuizData();
      renderQuiz(imgUrl, correctAnswer, choices);
```

## Challenges: 

challenge 1: 

```JS

```


