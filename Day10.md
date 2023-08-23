# Day 10


## I Learned: 

- call back queue
- Event Loop
- Promises
  

## Code Snippets:

Important Code: 
```JS

```

## challenges:

challenge 1:

```JS
const executeInSequenceWithCBs = (tasks, callback) => {
  const results = [];
  
  const executeNextTask = (index) => {
    if (index >= tasks.length) {
      callback(results);
      return;
    }
    
    tasks[index]((message) => {
      results.push(message);
      executeNextTask(index + 1);
    });
  };
  
  executeNextTask(0);
};
```


challenge 2:

```JS
const executeInParallelWithPromises = async (apis) => {
  const promises = apis.map(api => fetch(api.apiUrl)
    .then(response => response.json())
    .then(data => ({
      apiName: api.apiName,
      apiUrl: api.apiUrl,
      apiData: data
    }))
  );

  return Promise.all(promises);
};
```


challenge 3:

```JS
const executeInSequenceWithPromises = async (apis) => {
  const results = [];
  
  for (const api of apis) {
    const response = await fetch(api.apiUrl);
    const data = await response.json();
    
    results.push({
      apiName: api.apiName,
      apiUrl: api.apiUrl,
      apiData: data
    });
  }
  
  return results;
};
```
