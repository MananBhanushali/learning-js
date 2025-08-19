# Event Listeners in JavaScript

```js
element.addEventListener(event, funcName);

// To Remove an Event Listener 
element.removeEventListener(event, funcName);
```

For Example :

```js
const buttonElement = document.querySelector('.button-classname');

const func = () => {
    console.log('Click Registered');
};

buttonElement.addEventListener('click', func);

buttonElement.removeEventListener('click', func);
```