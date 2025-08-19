# Basics of JavaScript

## Hello World

```javascript
console.log('Hello World'); // Types Hello World in the Console
```

To send an Alert(Popup)
```javascript
alert('Hello World');
```

## Strings

```javascript
console.log('Number of Items : ${1 + 1}') // Formatted String
> 'Number of Items : $2'
```

### String Methods and Properties

```javascript
console.log('hello'.length);
>5

console.log('hello'.toUpperCase());
>'HELLO'
```

## Variables

Defined as : **let \<name> = data;**

Can also be Defined as : **var \<name> = data;**

**While reassigning(modifying) a variable, there is no need to use let.**

### Constant Variables (Cannot change values later)

Defined as : **const \<name> = data;**

```javascript

let var1 = 2;

console.log('Number of Items : ${var1}');
> 'Number of Items : $2'

var1 = var1 + 2;
console.log(var1);
>4
```

### typeof Variables

typeof \<variable-name> gives us the datatype of the variable

```javascript

let var1 = 2;
let var2 = 'hello';

console.log(typeof var1);
> number

console.log(typeof var2);
> string

```

## Boolean Values ( true and false )

### Comparision Operators

\> - greater than  
< - less than  
\>= - greater than or equal to  
<= - less than or equal to  
**== - loose equality comparision ( allows type coercien )  
=== - strict equality comparision  
!= - loose inequality comparision ( allows type coercien )  
!== - strict inequality comparision**. 

>[!NOTE]
== and != allow type coercien

```javascript
console.log(5 == "5");   // true (the string "5" is coerced to the number 5)
console.log(0 == false); // true (false is coerced to 0)
console.log(null == undefined); // true (special case where they are considered loosely equal)
console.log(10 == "abc"); // false (no meaningful coercion possible)
```

### Logical Operators
&& - Logical AND  
|| - Logical OR  
! - Logical NOT 

## If Else Statements

```javascript
if (condition1) {
    code1 
} else if (condition2) {
    code2 
} else {
    other-code 
}
```

### Ternary Operators ( Shortcut way of If-Else )

```javascript
const result = condition ? 'isTrue' : 'isFalse'; 
```

It returns 'isTrue' if condition is true, or 'isFalse' if condition is false ( stops early ).  
**The result of a Ternary Operation can be stored in a variable.**

### Guard Operator ( Short Circuit of AND Operator )

In a Logical AND statement, if the First Condition is false, then the second condition is not checked.

```javascript
const message = false && 'hello'; // will not execute second statement
console.log(message);
>false

const message2 = 5 && 'hello'; 
console.log(message2);
>'hello'
```

### Default Operator ( Short Circuit of OR Operator )

In a Logical OR statement, if the First Condition is true, then the second condition is not checked.

```javascript
const message = 'EUR' || 'USD'; // will not execute second statement
console.log(message);
>'EUR'

const message2 = undefined || 'USD'; 
console.log(message2);
>'USD'
```

## Functions

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