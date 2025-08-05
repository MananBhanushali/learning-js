# Arrays in JavaScript

```javascript
const myArray = [10, 20, 30];

console.log(myArray[1]);
>20

myArray[1] = 15; 
console.log(myArray[1]);
>15
```

An Array can have any type of value inside
```javascript
[1, 5, 'hello', { name: 'manan' }, [3, 4]]
```

Array is a special type of object
```javascript
typeof([1, 2]);
>object
```

To check whether an object is an array
```javascript
console.log(Array.isArray([1, 2]));
>true
```

## Properties and Methods of Arrays

1. .length - Gives length of array
2. .push(value) - Adds a value to the end of Array
3. .splice(indexToRemove, numberOfValuesToRemove) - Removes the given number of values at the given index

```javascript
myArray = [10, 20, 30]

console.log(myArray.length)
>3

myArray.push(40) 
console.log(myArray)
>[10, 20, 30, 40]

myArray.splice(1, 2) // Removes 2 values at index 1
console.log(myArray)
>[10, 40]
```