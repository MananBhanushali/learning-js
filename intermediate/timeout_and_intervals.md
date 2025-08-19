# Timeouts and Intervals in JavaScript

### setTimeout(func, time)

Will run the function after the given time (in ms).  
Till then the next code will run ( Due to the Asynchronous Nature of JavaScript )

```js
setTimeout(function greeting() {
     console.log('hello');
     }, 3000); // will run after 3 seconds ( 3000 milliseconds )
```

### setInterval(func, interval)

Will run the function every interval ( multiple times ). 

**setInterval() returns a number ( an id ) which can be used to later stop the interval using clearInterval(ID).**

```js
const intervalID = setInterval(function greeting() {
     console.log('hello');
     }, 3000); // will run after every 3 seconds ( 3000 milliseconds )

clearInterval(intervalID);
```
