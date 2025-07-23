# Storing Data In JavaScript

- [Storing Data In JavaScript](#storing-data-in-javascript)
  - [JSON ( JavaScript Object Notation )](#json--javascript-object-notation-)
  - [Local Storage](#local-storage)
  - [Document Object Model ( DOM ) in JavaScript](#document-object-model--dom--in-javascript)


## JSON ( JavaScript Object Notation )

Difference between JavaScript Objects and JSON:
- JSON cannot store Functions
- In JSON, all the property names and values should be in double quotes.

To Convert JavaScript Object to JSON string: use **JSON.stringify(object)**
To Convert JSON string into JavaScript Object: use **JSON.parse(string)**

```javascript
const testObject = {
    name: 'test';
    price: 100;
    func: function test() {
        console.log('Function');
    }
}

const jsonString = JSON.stringify(testObject);
console.log(jsonString);
>{
    "name": "test", "price": 100
} // Function not present in JSON   

console.log(typeof jsonString);
>string

const newObject = JSON.parse(jsonString); // will not have function test()
```

## Local Storage 

To set Data in Local Storage: use **localStorage.setItem('\<name>', '\<value>')** ( only supports strings )

To get Data from Local Storage: use **localStorage.getItem('\<name>')**

To remove Data from Local Storage: use **localStorage.remove('\<name>')**

```javascript
localStorage.setItem('message', 'hello');

console.log(localStorage.setItem('message'));
>'hello'

localStorage.remove('message');
```

## Document Object Model ( DOM ) in JavaScript

The DOM combines HTML and JavaScript together, and hence gives JavaScript control over HTML

**Properties and Methods of document Object:**

```javascript
document.title = 'title';

// document.body contains: <body>...</body>
// typeof document.body returns object. Hence it is an object and has its own properties and methods

document.body.innerHTML = '<button>hello</button>'; // document.body.innerHTML gives all inner HTML, which can also be changed

console.log(document.querySelector('button')); // will return the first buttton element from the page
><button>hello</button> 
```

**Every Element has .innerHTML property , which can be used to view and edit its content.**

**To view the Inner Text, use the .innerText property.**

```javascript

document.body.innerHTML = '<button>hello</button>';

console.log(document.querySelector('button').innerText);
>hello

document.querySelector('button').innerText = 'changed'

console.log(document.querySelector('button').innerText);
>changed
```

>[!IMPORTANT]
To look for a particular element, assign it a class, and then use: **document.querySelector('.className')**

```javascript

document.body.innerHTML = `
<button class='first-button'>First</button>
<button class='second-button'>Second</button>
`;

console.log(document.querySelector('.second-button').innerHTML);
>Second
```

**element.classList.add('class-name') and element.classList.remove('class-name') can be used to add / remove classes from an element.**

**This can be used to change the appearance of an element on click, by giving it another class onclick, and then styling that class accordingly.**