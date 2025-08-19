# Functions in JavaScript

```javascript
function name() {
    console.log('hello');
}

// To call a function
name();
```

To use Return Values and Parameters :

```javascript
function name(parameter='default value') {
    return 'Hello ${parameter}' // function ends here. Lines after return are not executed
}

const varName = name('Manan');
console.log(varName);
>'Hello Manan'
```

>[!NOTE]

Functions can also be stored inside variables

```js
const funcVariable = function greeting() {
    console.log('hello');
};

console.log(funcVariable);
>f greeting() { console.log('hello' ) }

console.log(typeof funcVariable);
>function

// To run the function, call the variable
funcVariable();
>'hello'
```

Here, the name of the function is not needed, because the function can be accessed by the name of the variable.  
Such function which has no name is called an Anonymous function.

```js
const funcVariable = function() {
    console.log('hello');
};
```
