# Javascript Notes
____________________________________________________________________

## Console

The console is a panel that display important information for developers, like error messages. A lot of the work the computer does with our code is invisible by default, if we want to see things appear on our screen, we can print, or *log*, to our console directly.

In Javascript the `console` keyword refers to an object, or a collection of data and actions, that we can use in our code. Keywords are words that are buillt into the JS language so that the computer recognizes them and treats them specially.

One action, or *method*, that is built into the console object is the `.log()` method. When we write `console.log()` what we put inside the parentheses will get printed, or logged, to the console.

This can be very useful so what we can see the work that we are doing.
____________________________________________________________________

## Comments

Comments are a way to add text to a coding document that does not directly affect the code itself. This is useful for reminding yourself what certain lines of code do as well as informing any one else who didnt write the code, what is going on in the code.

There are *two ways* to write a comment in JS.

If a comment only takes up a single line it can be denoted by double forward slashes `//`

```
// Prints to the console
console.log(5);
```
When the code is executed, "5" will be printed to the console. The text that follows the double slashes `//` is only there to remind developers what is going on.

If a comment takes up *multiple lines* then we need to encompass the comment with `/*` and `*/`

```
/* This is a comment
This is the next line of the comment
And so on and so forth */
console.log(5);
```

You can also use this method to comment something out in the middle of a line of code, for example:

```
console.log(/*comment*/ 5); //Still just prints 5
```
____________________________________________________________________

## Data Types

Data Types are the classifications we give to the different kinds of data that we use in programming. In JavaScript there are seven fundamental data types:

- `Numbers` any number, including decimals
- `String` any grouping of characters on your keyboard which must be surrounded by quotes `' '` or double quotes `" "`
- `Boolean` can be either `true` or `false` and is not surrounded by quotes
- `Null` this represents the intentional absence of data
- `Undefined` this represents the absence of a value however it is different than `null` in that it is just the absence of a value and typically not intentional.
- `Symbol` a newer feature of the language, symbols are unique identifiers useful in more complex coding which we won't cover just yet.
- `Object` a collection of related data (You've done UE4 projects you know what an object is)
____________________________________________________________________

## Arithmetic Operators

Things like addition `+`, subtraction `-`, multiplication `*` and division `/` and modulo `%` are all arithmetic operators. 

```console.log(3+5); //prints 8```

The remainder operator, or *modulo*, returns the number that remains after the right hand number divides the left hand number. Example:

```console.log(11 % 3);``` //prints "2" because 3 can fit into 11 three times with a remainder of 2.

## String Concatenation

We can add strings together with a `+` operator, example:

```console.log('hi' + 'ya"); //prints "hiya"```
____________________________________________________________________

## Properties

All data types have access to specific properties that are passed down to each instance of the data. For example, all strings have a property called length that stores the number of characters in the string. You can get that property information by appending the string with a period and the property name

```console.log('Hello".length); //Prints 5 because there are 5 letters in Hello.```

The `.` is also an operator - the dot operator - which we will cover a bit more into these notes.
____________________________________________________________________

## Methods

Methods are actions that we can perform. Data types have access to specific methods that allow us to handle instances of that data type. We can use, or *call*, these methods by appending an instance with:
- a dot operator `.`
- the name of the method
- opening and closing parenthesis

``'example string'.methodName();```

Previously, we've used the `.log()` mtehod for the `console` object.

```
console.log('hello'.toUpperCase()); //prints "HELLO"
console.log('Hey').startsWith(H)); //prints true
```

JavaScript is *case sensitive* so methods such as `toUpperCase` and `startsWith` must be written exactly as they are shown.
____________________________________________________________________

## Built in Objects

JS has built in objects, such as `console`, as well as many others. For example, JS also has a built in `Math` object which has built in methods.

```console.log(Math.random());  //prints a random number between 0 and 1```

If we wanted to get a number between 0 and 50, we could write

```Math.random() * 50;```

which would take the answer and multiply it by 50, however its likely that this could return a decimal. To ensure that the answer is a whole number, we can take advantage of another useful math method called `floor`.

`Math.floor();` takes in a decimal number and rounds down to the nearest whole number.

```console.log(Math.floor(Math.random() * 10);```

`Math.random() * 10` gives a number between 0 and 10 and `Math.floor` ensures that the number will be a whole number.
____________________________________________________________________

## Declaring Variables

We can use the keywords `var`, `let`, or `const` to declare a variable.

```
var myName = 'Kawika';
let myAge = 30;
const myEyes = "Brown";
```

The keyword `var`, `let`, and `const` tells the computer that we are declaring a variable and "myName" is the *name of the variable*. Then we use the assignment operator, `=`, to assign a value to the declared variable.

It is also common to use *camelCasing* within JavaScript. This is because we cannot use spaces in variable names so we smush them all the words in a variable name together. The first word will be lower case and any word that follows that will have the first letter capitalized, i.e. `mySuperLongVariableName`

- Variable names *CAN NOT* start with numbers
- Variable names *ARE* case sensitive; 'myName' and 'myname' would be different variables.
-Variable names *CAN NOT* have a name that is the same as any keyword in JS.

Typically, `var` is not used any more but you may still encounter it in legacy code so its good to know. Instead, we more commonly use the keywords `let` and `const`.

A variable declared with `let` allows the value to change once they have initially been declared and given a value. They *can* be declared without assigning a value and if so the value would be `undefined`.

`const` on the other hand, are variables that are *constant* and therefore *can not* be changed once the value is assigned.
____________________________________________________________________

## Mathmatical Assignment Operators

So, we *can* do things like 

```
let w = 4;
w = w + 1;

console.log(w); //prints 5
```

However, we can accomplish the same thing with *mathmatical assignment operators*.

```
let w = 4;
w += 1;
console.log(w); //Also prints 5
```

The `+=` math assignment operator performs the operation of the first operator, `+`, using the number to the right and then reassigns the computed value to `w`. Similar things can be accomplished with `-=`, `/=`, and `*=`
____________________________________________________________________

## Increment and Decrement Operators

These can be used to increase `++` or decrease `--` a number value by 1. When we use these operators the value is updated and assigned as the new value of that variable.

```
let a = 10;
a++; //Prints 11

let a = 10;
a--; //Prints 9.
```
____________________________________________________________________

## String Concatenation with Variables

Previously we learned that we can combine strings with other strings by what is known as string concatenation. We can do similar things with variables.

```
let myPet = 'Shiba Inu';
console.log ('I own a pet ' + myPet + '.');
//Prints "I own a pet Shiba Inu."
```
____________________________________________________________________

## String Interpolation

In the ES6 version of Javascript we can insert, or interpolate, variables into strings using *template literals*.

```
const myPet = "Shiba Inu";
console.log(`I own a pet ${myPet}.`);
```

Notice that a template literal is wrapped in backticks (the key to the left of the 1 key; also the tilde key)

Inside the template literal you will see a placeholder, ${varName}. The value of whatever variable is referenced will be inserted here.
____________________________________________________________________

## Typeof Operator

We can use the `typeof` operator to determine what kind of data type our variables are.

```
const unknown1 = 'foo';
console.log(typeof unknown1); // Prints string

const unknown2 = 10;
console.log(typeof unknown2); //Prints "number"

const unknown3 = true;
console.log(typeof unknown3); //Prints boolean
```
____________________________________________________________________

# Conditionals

Conditionals are used to determine if a certain condition or conditions are met, and if they are, then a certain code block will fire off. If the condition is *not* met, then a different code block will fire. One of the most common conditional is the `if` statement. 

We can use comparison operators `===` to check if a value is true or false

```if (var === true) { // do stuff }```

Or we can just type the name of the variable and the code will execute only *if* it returns `true`; If it returns `false` it will not.

```if (true) { // do stuff }``

`else` statements can also be used to execute a separate block of code if the condition check does not meet our criteria.

```
if (false) { //do a thing };
else { // do a different thing};
```

`else` conditionals must be paired with an `if` statement and when used together they are referred to as an `if...else` statement. When a solution can only be answered "yes" or "no" (read: "true" or "false") these are known as *binary decisions*.
____________________________________________________________________

## Comparison Operators

When writing conditional statements sometimes we need to use different types of operators to compare values. These are *comparison operators*. These operators compare the value on the left with the value on the right. For example `10 < 12` would be `true` because 10 is less than 12.

- `<` less than
- `<=` less than or equal to
- `>` greater than
- `>=` greater than or equal to
- `===` is equal to
- `!==` is not equal to

In practice, it can look like this:

```
if (x >= y) {
    //do stuff
}
else {
    // do different stuff
}
```
____________________________________________________________________


## Logical Operators

These are things like the *and* operator `&&`, the *or* operator `||`, and the *not* operator `!` and they can be used in your `if...else` conditional checks as well.

`&&` checks to make sure all criteria values are true

```
if (stopLight === 'green' && pedestrians === 0) {//do stuff};
else {// do other thing};
```

`||` checks to make sure at least one of the conditions returns true

```
if (day === 'Saturday' || day === 'Sunday') {//do thing};
else {//do stuff};
```

`!` checks to see if the returned value is the *opposite*. Essentially, it negates, or reverses, the value of the boolean.

```
let excited = true;
console.log(!excited); //prints false

let sleepy = false;
console.log(!sleepy); //prints true
```
____________________________________________________________________

## Truthy and Falsy

Sometimesd we want to evaluate a condition check with non-boolean data types like strings and numbers. Sometimes you'll want to check if the variable exists and if it has a value, and not necessarily care about what the value is.

If a variable exists and has a value, we say that it has a *truthy* value, meaning that the variable exists and it does hold a value but that value is not the boolean value of `true`.

Examples of a *falsy* value would be things like:

- Has a number value of 0
- The number value is NaN (not a number)
- Is an *empty string* `''` or `""`. Note that if there is even ONE SPACE in between the quotes the string will be evaluated as truthy. To be evaluated as falsy there **must be no spaces between the quotes**.
- The value is `null` or `undefined`
____________________________________________________________________

## Truthy and Falsy Assignment

Say you have a website and want to take a user’s username to make a personalized greeting. Sometimes, the user does not have an account, making the username variable falsy. The code below checks if username is defined and assigns a default string if it is not:

```
let username = '';
let defaultName;
 
if (username) {
  defaultName = username;
} else {
  defaultName = 'Stranger';
}
 
console.log(defaultName); // Prints: Stranger
```

If you combine your knowledge of logical operators you can use a short-hand for the code above. In a boolean condition, JavaScript assigns the truthy value to a variable if you use the `||` operator in your assignment:

```
let username = '';
let defaultName = username || 'Stranger';
 
console.log(defaultName); // Prints: Stranger
```

Because `||` statements check the left-hand condition first, the variable defaultName will be assigned the actual value of username if it is truthy, and it will be assigned the value of 'Stranger' if username is falsy. This concept is also referred to as *short-circuit evaluation*.
____________________________________________________________________

## Ternary Operator

In the spirit of using short-hand syntax, we can use a ternary operator to simplify an `if...else` statement.

Take a look at the `if...else` statement example:

```
let isNightTime = true;
 
if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
```

We can use a ternary operator to perform the same functionality:

```
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```
In the example above:

- The condition, `isNightTime`, is provided before the `?`
- Two expressions follow the `?` and are separated by a colon `:`
- If the condition evaluates to `true`, the first expression executes.
- If the condition evaluates to `false`, the second expression executes.

Like `if...else` statements, ternary operators can be used for conditions which evaluate to true or false.
____________________________________________________________________

## Else If

`else if` statements are used if we have more than two options in our `if...else` statements. You can add as many `else if` statements as you need but just remember that `if` statements come first, then `else if`, and the final one is `else`.

```
let groceryItem = 'papaya';
 
if (groceryItem === 'tomato') {
  console.log('Tomatoes are $0.49');
} else if (groceryItem === 'papaya'){
  console.log('Papayas are $1.29');
} else {
  console.log('Invalid item');
}
```
____________________________________________________________________

## Switch

The `switch` keyword and its syntax can be used instead of if/else if/else statements and is typically easier to read and write.

```
let groceryItem = 'papaya';
 
switch (groceryItem) {
  case 'tomato':
    console.log('Tomatoes are $0.49');
    break;
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
}

// Prints 'Papayas are $1.29'
```
The `switch` keyword initiates the statement and is followed by parentheses `()` which contains the value that each `case` will compare.

Inside the curly bracket block `{}` there are multiple cases. The `case` keyword checks if the expression matches the specified value that comes after it.

The `break` keyword tells the computer to exit the `switch` block and to not check any more cases or execute any more code inside the code block. Without the `break` keyword, the first matching case will run and so will every subsequent case regardless of whether or not it matches.

This behavior is different from `if...else` conditional statements that execute only one block of code.

At the end of each `switch` statement there is a `default` statement which will run if none of the `case` conditions evaluate to true.
____________________________________________________________________

# Functions

We declare functions in a similar way to declaring variables, the syntax being

```
function identifier (//inputs go here) { // code to execute goes here };
```

the first part, or the function keyword, lets us know that we are declaring a function, the following part, identifier, is the name of the function, and the stuff inside the curly brackets is what the function does.
____________________________________________________________________

## Hoisting

This refers to when we call a function before declaring it. While this will still work, it is no considered good practice.
____________________________________________________________________

## Calling A Function

We can call a function by typing the function identifier/name followed by parenthesis and a semicolon. 

```myFunction()```

When you call a function it executes the function body (all the stuff between the curly brackets).
____________________________________________________________________

## Parameters and Arguments

Some functions might need some kind of input in order to function properly. When we declare a function we can specify its *parameters*, these allow functions to accept inputs and perform the body code using the inputs. 

The parameters are placeholders for information that will be passed into the function when it is called.

```function theFunctionName (parameter1, parameter2, parameterEtc) {
//function body goes here
};
```

When we call a function and use values in the parenthesis(e.g. using your name as parameter1, your age as parameter2, etc) they are called *arguments*. 

Arguments can be raw values or the variable names themselves. The order that the parameters are declared is the order that the arguments need to be input. For example, if the parameters of a function are `(height, width)` and we use the arguments `(10, 6)` the `10` value will be the `height` and the `6` will be the `width`. 

If we had variables called `squareHeight` and `squareWidth` we could also use `(squareHeight, squareWidth)` as the arguments in the function as well.
____________________________________________________________________

### Default Parameters

A feature of ES6 is the ability to use default parameters. These are predetermined values in case no argument is passed into the function or if the argument is undefined when called.

```
function multiply(a, b = 1) {
  return a * b;
}

multiply(5)
//since a second argument was not passed in, the function will multiply 5 and 1. 5 is the a value, and the default value of 1 will be used for b.

multiply(5, 2)
//since we passed a second argument, the function will multiply 5 and 2.
```
____________________________________________________________________

## Return

When a function is called the computer goes thru the code and evalutes the result of the function. This is the `return` value. By default the value is undefined. Consider the following code:

```
function rectangleArea(width, height) {
  let area = width * height;
}
console.log(rectangleArea(5, 7)) // Prints undefined
```

This prints undefined because we didnt use a `return` keyword/statement. To create a return statement we use the `return` keyword followed by the name of the value we wish to return. 

When a return statement is used in a function body, the execution of the function is stopped and the code that follows it within the body will not be executed.

```
function rectangleArea(width, height) {
  let area = width * height;
  return area;
  console.log('This line of code will not be executed');
}

console.log(rectangleArea(5, 7)) // Prints 35
```
____________________________________________________________________

## Helper Functions

We can also use the return value of a function inside of another function. These functions being called within another function are often referred to as helper functions. Since each function is carrying out a specific task, it makes our code easier to read and debug if necessary.

```
function multiplyByNineFifths(number) {
  return number * (9/5);
};
 
function getFahrenheit(celsius) {
  return multiplyByNineFifths(celsius) + 32;
};
 
getFahrenheit(15); // Returns 59

```
____________________________________________________________________

## Function Expressions

Another way to define a function is to use a *function expression*. A function expression is often stored in a variable in order to refer to it.

To define a function inside an expression we use the `function` keyword. In a function expression, the function name is usually omitted. A function with no name is called an *anonymous function*.

```
const calculateArea = function (width, height) {
	const area = width * height;
	return area;
};
```

We declare a variable, the variables name is the identifer of your function. Since the release of ES6 its common practice to use `const` as a keyword to declare the variable.

An anonymous function is assigned as that variable's value. We include possible parameters as well as the function body in curly braces as well.

To invoke a function expression write the name of the variable followed by parentheses enclosing any arguments being passed into the function.

```variableName(argument1, argument 2)```

Unlike function declarations, function expressions **are not hoisted** so they cannot be called before they are defined.
____________________________________________________________________

## Arrow Functions

ES6 introduced *arrow function* syntax. A shorter way to write functions by using the special "fat arrow" notation `() =>`

Arrow functions remove the need to type of the keyword `function` every time you create a function. Instead, you first include the parameters inside the parenthesis and then add an arrow `=>` that points to the function body surrounded by curly brackets `{ }`.

```
const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
}
// Arrow function
```
Is the same function as

```
const rectangleArea = function (width, height) {
  let area = width * height;
  return area;
}
// Function expression
```

Or even

```
function rectangleArea (width, height) {
  let area = width * height;
  return area;
}
// "Regular" function
```
____________________________________________________________________

### Concise Body Arrow Functions

Javascript also provides several ways to refactor arrow function syntax. The most condensed form of the function is known as concise body.

1. Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a funciton takes zero or multiple parameters, parentheses are required.

```
const funcName = () => {}; // used for zero parameters

const funcName = paramOne => {} ; // used for a single parameter

const funcName = (paramOne, paramTwo) => {}; // used for two or more parameters
```

2. Function bodies composed of a single-line block does not need curly braces. Without curly braces, whatever that line evaluates will be automatically returned. The contents of a block should immediately follow the arrow => and the return keyword can be removed. This is reffered to as *implicit return*.

```
const sumNumbers = number => number + number; 
```
No need for curly brackets or return statement. Function will return value of number + number. This is a *single-line block*

```
const sumNumbers = number => {
  const sum  = number + number;
  return sum;
};
```
Has a return statement and the function body is enclosed in curly brackets.

____________________________________________________________________

# Scope

This refers to where variables can be accessed or referenced. Some variables can be accessed from anywhere in the program, while some are only available under certain context.

Some things are *globally* accessible, while others are *locally*. Think about the sky & the stars, they are globally visible(accessible) to everyone but the things in your city are locally visible(accessible).
____________________________________________________________________

## Blocks and Scope

Blocks of code are the things inside of curly braces. They help us group one or more statements together and serve as an important structural marker for our code.

```
const myFunc = () => {
    // this is the block of code for myFunc
}
```
____________________________________________________________________

### Global Scope

These are things that are declared outside of the blocks also known as *global variables*. Because they are not nested inside of any block they can be accessed by any code in the program, including code in blocks.

```
const name = 'Kawika';

const myFunc = () => {
  console.log(name);
}
// This will log my name to the console
```
____________________________________________________________________

### Block Scope

This refers to when a variable is defined within a block fo code, and when it is, that variable is only accessible within that block of code. These are also known as *local variables*

```
const myFunc = () => {
  let favoriteFood = 'pizza';
  console.log(name);
}
// this will log 'pizza' to the console.

const anotherFunc = () => {
  console.log(favoriteFood);
}

// this function does not have access to the variable 'favoriteFood' and will not log 'pizza' to the console.
```
____________________________________________________________________

## Scope Pollution

This refers to when we have too many global variables that exist in the global namespace, or when we reuse variables across different scopes. This makes it difficult to keep track of our different variables and sets us up for potential accidents. For example, if we define 'num' as a global variable but then also define a local variable 'num' inside of a function, this will case confusion/issues, and will override the global 'num' with whatever the value is in our function where we define 'num' locally.

**Best Practices** for scoping variables will greatly improve your code in several ways:
- More legible since blocks will organize your code into discrete sections
- Makes you code more understandable since it clarifies which variables are associated with different parts of the program rather than having to keep track of them line after line.
- Easier to maintain code, since it will all be modular.
- Save memory in your code because it will cease to exist after the block finishes running.

____________________________________________________________________

# Arrays

These are kind of like a list and they store data types in an ordered manner.

```
const myArray = [ 1, 2, 3, 4, 5];

const anotherArray = [ 'pizza', 'tacos', 'burgers']
```
____________________________________________________________________

## Array Literal

We create an array by wrapping items in square brackets `[ ]`. Arrays can hold data of all the same type or different data types.

We can create an array by itself or set the array as a value to a variable. Each entry in an array is referred to as an *element*.

Each element has its own unique identifiying number, or *index*, that signifies its location in the array. We can use the indexes to access individual items from the array. Arrays in JS are *zero-indexed*, meaning they start at 0 instead of at 1. To access a individual element from an array, you would use the syntax:

```array[0]```

Where "array" is the name of the array and the `0` is the index of whatever element you want access to. We can also set a variables value to an individual element from an array. For example

```
const array = ['thing', 'stuff', 'blahblah'];
let variable = array[2]; //sets variable value to 'stuff'
```

You can also access individual characters in a string with a similar method. For example

```
const hello = 'Hello World';
console.log(hello[6]);
// Output: W
```

If you try to access an element that does not exist (i.e. the array has 3 elements and you try to access the fourth element) it will return `undefined`.

____________________________________________________________________

## Updating Elements


If we want to update/change an element in an array we can do so using the syntax:

```array[3] = 'new value';```

This will overwrite whatever element is in the array at index 3 with whatever the new value is.
____________________________________________________________________

## Arrays with `let` and `const`

`let` variables allow us to change the variable value while `const` does not. 

However, elements in an array declared with const remain mutable(changeable). We can change the contents of a const array, but cannot reassign a new array or a different value.

If we create an array with the `let` keyword, we can update an element in the array or change the entire array itself. For example:

```
let condiments = ['Ketchup', 'Mustard', 'Soy Sauce', 'Sriracha']; //declare array
condiments[0] = 'Mayo'; //change first element from ketchup to mayo
condiments = ['Mayo']; //change entire array to only have 1 element, 'mayo'.
```

If we create an array with the `const` keyword, we can update/change an element in the array but we **cannot** change the entire array itself.

```
const drinks = ['Milk', 'Juice', 'Water', 'Soda']; //declare array
drinks[0] = 'Beer'; //we CAN do this
drinks = ['Beer']; //we CANNOT do this
```
____________________________________________________________________

## Array Length Property

The `length` property is built in to all arrays and allows us to return the number of items in an array by using dot notaiton and the keyword `length`.

```
const myArray = ['red', 'blue', 'green'];
console.log(myArray.length) //logs "3" to the console
```
____________________________________________________________________

## Array `.push` Method

This allows us to add items to the end of an array by using dot notation and the keyword `push` and then putting whatever value we wish to add to the array in parentheses.

```shoppingList.push('apples', 'napkins');```

Sometimes this is referred to as a *destructive array method* because it changes the initial array.
____________________________________________________________________

## Array `.pop` Method

This allows us to remove the last item from an array by using dot notation and the keyword pop, followed by parentheses. It does not take any arguments and the value that is removed is stored in the variable "removed" if we want to use it later.

```shoppingList.pop()```

____________________________________________________________________

## More Array Methods

Other methods besides `.push()` and `.pop()` exist which we can find in the JS array documentation online. Some methods include .join(), .slice(), .splice(), .shift(), .unshift(), and concat() amongst many others.

`.push()` and `.pop()` both mutate the array on which they are called however there are times where we dont want to mutate the original array and we can use non-mutating array methods. 

- `.shift()` will remove the first item from the array

- `.unshift()` will add an element to the beginning of the array, the element being whatever argument you insert between the parentheses.

- `.slice()` returns a new array that contains the elements specified by the first argument and all subsequent elements up to, but not including, the second argument. we can use keywords like start and end for the arguments or we can also use indexes. 

- `.indexOf()` finds the index of whatever element we specify within the argument parentheses.

- `.splice(start, itemCount, item1, item2, ...., itemN)`;
	- `start`: The array index at which the insertion and/or removal is to begin.
	- `itemCount` (optional): The number of elements in the array to remove beginning at start.
	- `item1, item2,..., itemN` (optional): The elements that will be inserted into the array at start.
____________________________________________________________________

## Nested Arrays

This is what we call it when an array has another array or multiple arrays inside of it.

```const nestedArr = [[1], [2, 3]];```

`nestedArr` is an array with two arrays inside of it, one array with a length of 1 containing the number 1, and the second array contains the numbers 2 and 3.

To access nested arrays we can use bracket notation with an index value just like we access any other element.

```nestedArr[1]; //will access the array containing 2 and 3.```

If we wanted to access indexes within that array we can chain bracket notation with index values.

```
nestedArr[1][0]; //access the array containing 2 and 3 and then accesses the first element (index 0) of that array.
```
____________________________________________________________________

# Loops

Loops are repeated until a specific condition, known as a *stopping condition*, is reached. You'll also hear the term "iterate" when referring to loops, meaning "to repeat". 

Loops iterate, or repeat, until the stopping condition is met.
____________________________________________________________________

## For Loops

A `for` loop typically includes an iterator variable that appears in all three expression. The iterator variable is initialized, checked against the stopping condition, and assigned a new value on each loop iteration. You can name the iterator variable anything you want but its best practice to use a descriptive name.

```
for (let counter = 0; counter < 4; counter++) {
  console.log(counter);
}
```
This code inside the parentheses `()` is basically saying:

"When we start the loop, we will initialize the variable `counter` and set its value to `0`. The loop will continue to run/iterate as long as `counter` is less than `4` and every time the loop finishes an iteration we will increment `counter` by `1`."

A `for` loop contains three expressiones separated by `;` inside the parentheses `()`

1. an initialization starts the loop and can also be used to declare the iterartor variable
2. stopping condition which the iterator variable is checked against. if the condition evaluates `true` the code block will run, if its `false` it will stop.
3. an iteration statement is used to update the iterator variable on each loop.

____________________________________________________________________

### Looping in Reverse

What if we want the loop to count backwrads? to run a backward for loop we must:
1. set the iterator variable to the highest desired value in the intialization expression
2. set the stopping condition for when the iterator variable is less than the desired amount
3. set the iterator to decrease after each iteration.
____________________________________________________________________

## Looping Through Arrays

We can use a `for` loop to perform the same operation on each element in an array. To loop through each element in an array, a `for` loop should use the array's `.length` property in its condition. Example:

```
const animals = ['Grizzly Bear', 'Sloth', 'Sea Lion'];
for (let i = 0; i < animals.length; i++){
  console.log(animals[i]);
}
```
____________________________________________________________________

## Nested Loops

This is what we call loops running inside another loop. Once use for nested loops would be to compare the elements in two arrays. For each round of the outer loop, the inner loop will run completely thru. Example:

```
const myArray = [6, 19, 20];
const yourArray = [19, 81, 2];
for (let i = 0; i < myArray.length; i++) {
  for (let j = 0; j < yourArray.length; j++) {
    if (myArray[i] === yourArray[j]) {
      console.log('Both arrays have the number: ' + yourArray[j]);
    }
  }
}
```

For each element in the outer loop array, myArray, the inner loop will run in its entirety comparing the current element from the outer array, `myArray[i]`, to each element in the inner array, `yourArray[j]`. When it finds a match, it prints a string to the console.

Another example:

```
let bobsFollowers = ['linda', 'gene', 'louise', 'tina'];
let tinasFollowers = ['gene', 'louise', 'jimmyjr'];
let mutualFollowers = [];

for (let i=0; i < bobsFollowers.length; i++) {
  for (let j=0; j < tinasFollowers.length; j++) {
    if (bobsFollowers[i] === tinasFollowers[j]) {
      mutualFollowers.push(tinasFollowers[j]);
      console.log(mutualFollowers[j]);
    }
  }
};
```
____________________________________________________________________

## While Loops

These are similar to `for` loops but use a different syntax. The `while` loop is ideal when you dont know in advance how many times the loop should run.

```
// A while loop that prints 1, 2, and 3
let counterTwo = 1;
while (counterTwo < 4) {
  console.log(counterTwo);
  counterTwo++;
}
```

1. The iteration variable is declared before the loop so it has a global scope and we can access it inside our loop.
2. We start the loop with the keyword `while` followed by a stopping condtion, or test condition. This is checked before each iteration of the loop. While its `true`, the block will continue to run. When it is `false`, the loop will stop.
3. Then we have our loops code block which fires off every time the loop iterates.
____________________________________________________________________

## `Do...While`

`do...while` statements say to do a task once and then to keep doing it until a specified condition is no longer met. The syntax looks like:

```
let countString = ' ';
let i = 0;
 
do {
  countString = countString + i;
  i++;
} while (i < 5);
 
console.log(countString);
```

`while` and `do...while` are different because the `do...while` loops will run *at least once* whether or not the condition evalutes to true but the `while` loop will only run if the condition evalutes true.
____________________________________________________________________

## The `break` Keyword

This keyword, `break`, can be used to stop a loop before it reaches its stop condition. Example:

```
for (let i = 0; i < 99; i++) {
  if (i > 2 ) {
     break;
  }
  console.log('Banana.');
}
 
console.log('Orange you glad I broke out the loop!');
```
____________________________________________________________________

## Higher-Order Functions

When we are programming we need to be very explicit with the directions we give our programs. For example, when we tell another human "I baked a cake", they know that we had to preheat the oven, mix the ingredients, and set it in the oven for an amount of time and then remove it from the oven. This allows us to *abstract* away a lot of details and communicate key concepts more concisely. Instead of explicitly telling another person each step, we can just say "I baked a cake", and you understand all the implied details.

We'll learn how to use "abstraction" in programming by writing functions. In addition to allowing us to reuse our code, functions help to make clear, readable programs. If you encounter `countToThree()` you'll probably be able to guess what the function does without reading the function body.

We'll also learn a way to add another level of abstraction to our programming: *Higher-Order Functions*. 

These are functions that accept other functions as arguments &/o return a function as output. This allows us to build abstractions on other abstractions.
____________________________________________________________________

## Functions as Data

JavaScript functions behave like any other data type in the language, we can assign functions to variables and we can reassign them to new variables.

Lets say a function has a stupidly long name like 

```announceThatIAmDoingImportantWork()```

and if we had to call this function a bunch of times in our code it would hurt the readability of our JS document and just be irritating to have to constantly type out. What we can do, is assign this function as the value of a variable.

```const busy = announceThatIAmDoingImportantWork;```

and when we need to call that function, we can just type

```busy();```

the `busy` variable holds a *reference* to our original function. If we could look up the memory address for both `busy` and `announceThatIAmDoingImportantWork` they would point to the same place.

Notice that we assign the `announceThatIAmDoingImporantWork` without parentheses as the value to the `busy` variable.

In JavaScript, functions are *first class objects*, meaning that just like other objects you've encountered, Javascript functions can have *properties* and *methods*.

Since functions are a type of object, they have properties such as `.length` and `.name` and methods such as `.toString()`. You can read more about methods and properties of functions in the Javascript documentation. For instance, if we forgot what the original name of the function was, we could write

```console.log(busy.name);```

This would print our original function name in the console! Functions are special because we can invoke them (call them) but we can still treat them like any other data type.
____________________________________________________________________

## Functions as Parameters

Parameters are placeholders for data that gets passed into a function as an argument. Functions can accept other functions as parameters/arguments. 

**Higher Order Functions** are functions that either accepts functions as parameters, returns a function, or both.

**Callback Functions** are the name of the functions that get passed in as parameters.

When we call a higher-order function and pass another function in as an argument, *we do not invoke the argument function*.

Invoking the argument function would cause that function to run/evaluate and pass the return value of that function call. 

**With callback functions, we pass in the function itself by typing the name of the function without the parentheses.**

```
const higherOrderFunc = param => {
  param();
  return `I just invoked ${param.name} as a callback function!`
}
 
const anotherFunc = () => {
  return 'I\'m being invoked by the higher-order function!';
}
 
higherOrderFunc(anotherFunc);
```

In the above example, the `higherOrderFunc` accepts an argument, param. Inside the body of the `higherOrderFunc`, the param is invoked using parentheses, and finally a string is returned telling us the name of the callback funciton we passed in.

Below the higher-order function we have another function named `anotherFunc`. We then invoke the `higherOrderFunc` and pass in `anotherFunc` as the argument.

```
higherOrderFunc(() => {
  for (let i = 0; i <= 10; i++){
    console.log(i);
  }
});
````

In this example we invoke `higherOrderFunc` using an anonymous function as the argument. This is valid as anonymous functions can be used as arguments as well.

____________________________________________________________________

## Iterators

When we want to loop through, or iterate through, an array we can use things like the for loop. However, JS has built-in array methods which make looping easier.

These are called *iteration methods*, or sometimes known as *iterators*. These are methods called on arrays to manipulate elements and return values.
____________________________________________________________________

## The `.forEach()` Method

Invoked by using the method `.forEach()` this will execute whatever is in the code block for each element in an array. For example:

```groceries.forEach(function(groceryItem) {console.log('-' + groceryItem); });```

This will log a list of each grocery item to the console. Lets break down the syntax

- `groceries.forEach()` calls the `.forEach()` method on the `groceries` array
- `.forEach()` takes an argument of the callback function, `groceryItem()`.
- the `.forEach()` method then loops through the array and executes the callback functions for each element. During each execution, the current element is passed as an argument to the callback funciton.
- **The return value for `.forEach()` will always be `undefined`**.

Note that we can define the callback function either in the method or outside of it. We can use both regular function declaration syntax or arrow function syntax.

```groceries.forEach(groceryItem => console.log(groceryItem));```

Or

```
function printGrocery(element){
  console.log(element);
}
 
groceries.forEach(printGrocery);
```

Both do the same thing.
____________________________________________________________________

## The `.map()` Method

This can be invoked by using the `.map()` method. When it is called on an array, it takes an argument of a callback function and returns a new array. This works similarly to the `.forEach()` method but the major difference is that it returns a new array. 

For example:
```
const numbers = [1, 2, 3, 4, 5]; 
 
const bigNumbers = numbers.map(number => {
  return number * 10;
});
```

- In the example above, there is an array of integers called `numbers`
- `bigNumbers` will store the return value 
- `numbers.map()` will iterate thru each element in the numbers array and pass the element into the callback function.
- `return number * 10` is the code we execute on each element in the array.
____________________________________________________________________

## The `.filter()` Method

This can be invoked using the `.filter()` method. Like the map method, it returns a new array however it returns an array of elements **after filtering out certain elements from the original array**.

The callback function used as the argument for the filter method should return `true` or `false` depending on the element that is passed to it. When the callback function returns `true`, the corresponding element gets added to the new array.

```
const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 
 
const shortWords = words.filter(word => {
  return word.length < 6;
});
```

- We had an array `words`
- The new array `shortWords` is declared. This will store the returned array from the `.filter()` method invoked on the `words` array
- The callback function has a single parameter, `word`, and each element from the `words` array will be passed into the function as an argument
- `word.length < 6` is the condition in the callback function. Any word that is less than 6 characters will return truthy and be added to the new `shortWords` array.
____________________________________________________________________

## The `.findIndex()` Method

This can be invoked with the `.findIndex()` method. This method returns the index of the first element that evalutes `true` in the callback function.

```
const jumbledNums = [123, 25, 78, 5, 9]; 
 
const lessThanTen = jumbledNums.findIndex(num => {
  return num < 10;
});
```

- `jumpedNums` is our array of integers
- `lessThanTen` is the name of our new variable that will hold the value found with the `.findIndex()` method
- The callback function has a single parameter, `num`, and each element in the `jumbledNums` array will be passed into this function as the `num` argument.
- `num < 10` is the condition that we check the elements against. the`.findIndex()` method will return the index of the first element which evaluates `true` for that condition.
- If there isnt any element in the array that satisifies the condition in the callback function, the findIndex method will return `-1`.
____________________________________________________________________

## The `.reduce()` Method 

This can be invoked using `.reduce()` and it returns a single value after iterating through the elements of an array, thereby *reducing the array*. 

```
const numbers = [1, 2, 4, 10];
 
const summedNums = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue
})
 
console.log(summedNums) // Output: 17
```

- The first time this is executed (the first time this iterates) the element `1` will be used as `accumulator` and the element `2` will be used as `current value`. 
- The `return` statement adds these together and then the `.reduce()` method *removes* `1` and `2` from the array, and then replaces them with `3`. (This reduces the array length from 4 to 3; index0 = 3, index1 = 4, index2 = 10).
- When this code iterates a second time, it will use `3` and `4` as the `accumulator` and `currentValue` and then replace them with the value of `7`. (Reducing the array length from 3 to 2; index0 = 7, index1 = 10). 
- This keeps repeating until there is only one element left in the array.


The `.reduce()` method can also take an optional second parameter to set an initial value for `accumulator` (remember, the first argument is the callback function!). For instance:

```
const numbers = [1, 2, 4, 10];
 
const summedNums = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue
}, 100)  // <- Second argument for .reduce()
 
console.log(summedNums); // Output: 117
```
____________________________________________________________________

# Objects

At their core, objects are containers storing related data and functionality. Objects can be assigned to variables just like any JavaScript type. We use curly braces, `{}`, to designate an *object literal*.

```let spaceship = { }; //spaceship is an empty object```

We fill an object with *unordered data*. This data is organized into `key-value` pairs. A key’s `value` can be of any data type in the language including functions or other objects.

We make a `key-value` pair by writing the key’s name, or identifier, followed by a colon and then the value. We separate each key-value pair in an object literal with a comma, `,`. Keys are strings, but when we have a key that does not have any special characters in it, JavaScript allows us to omit the quotation marks:

```
let spaceship = {
	'Fuel type' : 'diesel',
	color: 'silver' 
};
```
____________________________________________________________________

## Accessing Properties - Dot Notation

There are a few ways we can access an objects properties, one of the ways is with *dot notation*. With dot notation you can write the objects name, followed by the dot operator, `.`, and then the property name (key). 

If we try to access a property that does not exist it will return `undefined`.

```spaceship.color; //returns silver```
____________________________________________________________________

## Accessing Properties - Bracket Notation

We've used bracket notation before when we access elements in an array. To use bracket notation to access an objects property, we pass in the property name (key) as a string.

```spaceship['Fuel Type'];```

**We must use bracket notation when**:

- Accessing keys that have numbers, spaces, or special characters in them.
- Accessing keys using a variable

Without bracket notation in these situations, our code would throw an error. 

This can be especially helpful when working with functions:

```
let spaceship = {
  'Fuel Type': 'Turbo Fuel',
  'Active Duty': true,
  homePlanet: 'Earth',
  numCrew: 5
};

let returnAnyProp = (objectName, propName) => objectName[propName];
 
returnAnyProp(spaceship, 'homePlanet'); // Returns 'Earth'
```

If we tried to write our `returnAnyProp()` function with dot notation (e.g. `objectName.propName`) the computer would look for a key of 'propName' on our object and not the value of the propName parameter.
____________________________________________________________________

## Property Assignment

Objects are mutable, meaning we can update/change them after we create them. We can use either dot notation or bracket notation and the assignment operator, `=`, to add a new `key-value` pair to an object OR change an existing property.

If the property already exists on the object, the original value will be replaced. 
If there was no property with that name, a new property will be added to the object.

It’s important to know that although we can’t reassign an object declared with `const`, we can still mutate it, meaning we can add new properties and change the properties that are there. 

*You can delete a property from an object with the delete operator*

```
const spaceship = {
  'Fuel Type': 'Turbo Fuel',
  homePlanet: 'Earth',
  mission: 'Explore the universe' 
};
 
delete spaceship.mission;  // Removes the mission property
```
____________________________________________________________________

## Methods

When the data being stored on an object *is a function* we call that a *method*. 

**A property is what an object has while a method is what an object does.** 

We can include methods in our object literals by creating ordinary, colon-separated key-value pairs. The key serves as our method’s name, while the value is an anonymous function expression.

```
const alienShip = {
  invade: function () { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};
```

With the new method syntax introduced in ES6 we can omit the colon and the function keyword.

```
const alienShip = {
  invade () { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};
```

If we wanted to call, or invoke, this method we would write

```alienShip.invade();```
____________________________________________________________________

## Nested Objects

Objects inside of objects inside of objects. Often times our objects may contain another object which might contain another object, each of these objects have key-value pairs. For example, if we have a `spaceship` object, we also have a `crew` object that contains all the crew members, but those crew members are also objects that have properties like `name` and `specialization`.

```
const spaceship = {
     telescope: {
        yearBuilt: 2018,
        model: '91031-XLT',
        focalLength: 2032 
     },
    crew: {
        captain: { 
            name: 'Sandra', 
            degree: 'Computer Engineering', 
            encourageTeam() { console.log('We got this!') } 
         }
    },
    engine: {
        model: 'Nimbus2000'
     },
     nanoelectronics: {
         computer: {
            terabytes: 100,
            monitors: 'HD'
         },
        'back-up': {
           battery: 'Lithium',
           terabytes: 50
         }
    }
}; 
```

We can chain operators to access nested properties. It can be helpful to pretend you are the computer and evaluate each expression from left to right so that each operation starts to feel a little more manageable.


```spaceship.nanoelectronics['back-up'].battery; // Returns 'Lithium'```
____________________________________________________________________

## Pass By Reference

Objects are passed by reference. This means when we pass a variable assigned to an object into a function as an argument, the computer interprets the parameter name as pointing to the space in memory holding that object. As a result, functions which change object properties actually mutate the object permanently (even when the object is assigned to a const variable).

```
const spaceship = {
  homePlanet : 'Earth',
  color : 'silver'
};
 
let paintIt = obj => {
  obj.color = 'glorious gold'
};
 
paintIt(spaceship);
 
spaceship.color // Returns 'glorious gold'
```

Our function `paintIt()` permanently changed the `color` of our spaceship object. However, reassignment of the spaceship variable wouldn’t work in the same way:

```
let spaceship = {
  homePlanet : 'Earth',
  color : 'red'
};
let tryReassignment = obj => {
  obj = {
    identified : false, 
    'transport type' : 'flying'
  }
  console.log(obj) // Prints {'identified': false, 'transport type': 'flying'}
 
};
tryReassignment(spaceship) // The attempt at reassignment does not work.
spaceship // Still returns {homePlanet : 'Earth', color : 'red'};
 
spaceship = {
  identified : false, 
  'transport type': 'flying'
}; // Regular reassignment still works.
```

Let’s look at what happened in the code example:

- We declared this `spaceship` object with `let`. This allowed us to reassign it to a new object with `identified` and `'transport type'` properties with no problems.
- When we tried the same thing using a function designed to reassign the object passed into it, the reassignment didn’t stick (even though calling console.log() on the object produced the expected result).
- When we passed `spaceship` into that function, obj became a reference to the memory location of the `spaceship` object, but not to the `spaceship` variable. This is because the `obj` parameter of the `tryReassignment()` function is a variable in its own right. The body of `tryReassignment()` has no knowledge of the `spaceship` variable at all!
- When we did the reassignment in the body of `tryReassignment()`, the `obj` variable came to refer to the memory location of the object `{'identified' : false, 'transport type' : 'flying'}`, while the `spaceship` variable was completely unchanged from its earlier value.
____________________________________________________________________

## Looping Thru Objects - `For...In`

We learned how to iterate through arrays using loops &/o iterative methods, but these methods rely on their numerical indexing and key-value pairs aren't ordered like arrays. Therefore, we need to use the `for...in` syntax.

`for...in` will execute a given block of code for each property in an object.

```
//our object
let spaceship = {
  crew: {
    captain: { 
      name: 'Lily', 
      degree: 'Computer Engineering', 
      cheerTeam() { console.log('You got this!') } 
    },
    'chief officer': { 
      name: 'Dan', 
      degree: 'Aerospace Engineering', 
      agree() { console.log('I agree, captain!') } 
    },
    medic: { 
      name: 'Clementine', 
      degree: 'Physics', 
      announce() { console.log(`Jets on!`) } },
    translator: {
      name: 'Shauna', 
      degree: 'Conservation Science', 
      powerFuel() { console.log('The tank is full!') } 
    }
  }
}; 
 
// for...in
for (let crewMember in spaceship.crew) {
  console.log(`${crewMember}: ${spaceship.crew[crewMember].name}`);
}
```

Our `for...in` will iterate through each element of the `spaceship.crew` object. In each iteration, the variable `crewMember` is set to one of `spaceship.crew`‘s keys, enabling us to log a list of crew members’ role and name.

____________________________________________________________________

# Advanced Object Concepts
____________________________________________________________________

## `this` Keyword

The `this` keyword is used when trying to access a calling objects properties. When we have an established object we can access its properties by using the syntax


```objectName.property;  /* OR */ objectName['property name'];```

But if we want to access the property of an object *within* the objects key-value pairs, we use the keyword `this` instead of the object name, for example

```this.property; /* OR */ this['property name'];```

A more thorough example:

```
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet() {
    console.log(dietType);
  }
};
goat.diet(); 
// Output will be "ReferenceError: dietType is not defined"
```

That’s strange, why is `dietType` not defined even though it’s a property of goat? That’s because inside the scope of the `.diet()` method, we don’t automatically have access to other properties of the goat object.

Here’s where the `this` keyword comes to the rescue. If we change the `.diet()` method to use the `this` keyword, the `.diet()` method works! :

```
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet() {
    console.log(this.dietType);
  }
};
 
goat.diet(); 
// Output: herbivore
```

The `this` keyword references the calling object which provides access to the calling object’s properties. In the example above, the calling object is `goat` and by using `this` we’re accessing the goat object itself, and then the `dietType` property of `goat `by using property dot notation.
____________________________________________________________________

## Arrow Functions and `this`

In the previous example we learned that for a method, the calling object is the object the method belongs to. If we use the `this` keyword in a method then the value of the `this` keyword is the calling object. However, when we use arrow functions for methods it gets a bit more tricky. Exmaple:

```
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet: () => {
    console.log(this.dietType);
  }
};
 
goat.diet(); // Prints undefined
```

Notice that this now prints `undefined` because its using an arrow function. That's because arrow functions inherently bind, or tie, an already defined `this` value to the function itself that is NOT the calling object. In the code above, the value of `this` is the *global object* (an object that exists in the global scope) which does not have a `dietType property` and therefore returns `undefined`.

**The key takeaway from the example is to avoid using arrow notation functions when using the `this` keyword in a method!**
____________________________________________________________________

## Privacy

Accessing & updating properties is fundamental when working with objects however sometimes we dont want other code to be able to access &/o update an objects properties at all. Thats where *privacy* comes into play. We can define which properties should and should not be changable.

Some languanges have built in privacy for objects but Javascript does not. JS developers use naming conventions to signal to other JS devs how to interact with a property. One common convetion is to place an underscore before the name of a property to signify that it should not be altered at all. For example

```
const bankAccount = {
_amount : 1000
};
```

However, even tho the underscore is there that **does not** prevent us from changing the value. This can cause unwanted side-effects when mutating objects and their properties.
____________________________________________________________________

## Getters

*Getters* are methods that get and `return` the internal properties of an object, but they can do more than just retrieve the value of a property.

```
const person = {
  _firstName: 'John',
  _lastName: 'Doe',
  get fullName() {
    if (this._firstName && this._lastName){
      return `${this._firstName} ${this._lastName}`;
    } else {
      return 'Missing a first name or a last name.';
    }
  }
}
 
// To call the getter method: 
person.fullName; // 'John Doe'
```

Notice that in the getter method above:

- We use the `get` keyword followed by a function.
- We use an `if...else` conditional to check if both `_firstName` and `_lastName` exist (by making sure they both return truthy values) and then return a different value depending on the result.
- We can access the calling object’s internal properties using this. In `fullName`, we’re accessing both `this._firstName` and `this._lastName`.
- In the last line we call `fullName` on person. In general, getter methods do not need to be called with a set of parentheses. Syntactically, it looks like we’re accessing a property.

Now that we’ve gone over syntax, let’s discuss some notable advantages of using getter methods:

- Getters can perform an action on the data when getting a property.
- Getters can return different values using conditionals.
- In a getter, we can access the properties of the calling object using `this`.
- The functionality of our code is easier for other developers to understand.

Another thing to keep in mind when using getter (and setter) methods is that properties cannot share the same name as the getter/setter function. If we do so, then calling the method will result in an infinite call stack error. One workaround is to add an underscore before the property name like we did in the example above.
____________________________________________________________________

## Setters

Setters reassign values of existing properties within an object. Example:

```
const person = {
  _age: 37,
  set age(newAge){
    if (typeof newAge === 'number'){
      this._age = newAge;
    } else {
      console.log('You must assign a number to age');
    }
  }
};
```

In this example we:
- Perform a check for what value is being assigned to `this._age`
- When we use the setter method, only values that are numbers will reassign to `this._age`
- There are different outputs depending on what values are used to reassign `this._age`

If we were to invoke the setter method

```
person.age = 40;
console.log(person._age); // Logs: 40
person.age = '40'; // Logs: You must assign a number to age
```

We can see that when we use a number it correctly reassigns the age to the new number, hwoever if we use 40 as a `string` data type it will not correctly reassign the new value.

Similarly to getter methods, we do not need to use parentheses when we call the setter method. Syntactically, it looks like we're assigning a new value to a property instead of invoking a function and passing the value in as an argument.

The advantages to using a setter are similar to a getter including checking input, performing actions on properties, and displaying a clear intention on how the object is supposed to be used. Nonetheless, it is still possible to directly reassign properties, for example

```person._age = 'fourty-five';```

Which would cause issues down the line, so be careful when reassigning values to objects. In this case, while the reassignment would be successful, the new value is a `string`, not a `number` data type - which could potentially cause errors since it is *supposed* to be a number.
____________________________________________________________________

## Factory Functions

Factory functions are used when we want to create many instances of an object quickly, rather than create multiple objects individually. A factory function is a function that returns an object and can be reused to make multple object instances and they can also have parameters which allow us to customize the object that gets returned. For example:

```
const monsterFactory = (name, age, energySource, catchPhrase) => {
  return { 
    name: name,
    age: age, 
    energySource: energySource,
    scare() {
      console.log(catchPhrase);
    } 
  }
};
```

This would allow us to use the `monsterFactory()` function and input different arguments with each call to produce unique instances of the object with each call. This way, we dont have to create an object literal for every monster we wish to create. We can just invoke the `monsterFactory()` function and input the necessary arguments.

____________________________________________________________________

## Property Value Shorthand

ES6 introduced some new shortcuts for assigning properties to variables known as *destructuring*.

In the previous exercise, we created a factory function that helped us create objects. We had to assign each property a key and value even though the key name was the same as the parameter name we assigned to it. To remind ourselves, here’s a truncated version of the factory function:

```
const monsterFactory = (name, age) => {
  return { 
    name: name,
    age: age
  }
};
```

Imagine if we had to include more properties, that process would quickly become tedious! But we can use a destructuring technique, called property value shorthand, to save ourselves some keystrokes. The example below works exactly like the example above:

```
const monsterFactory = (name, age) => {
  return { 
    name,
    age 
  }
};
```

Notice that we don’t have to repeat ourselves for property assignments!
____________________________________________________________________

## Destructured Assignment

We often want to extract key-value pairs from objects and save them as variables. Take for example the following object:

```
const vampire = {
  name: 'Dracula',
  residence: 'Transylvania',
  preferences: {
    day: 'stay inside',
    night: 'satisfy appetite'
  }
};
```

If we wanted to extract the `residence` property as a variable, we could use the following code:

```
const residence = vampire.residence; 
console.log(residence); // Prints 'Transylvania' 
```

However, we can also take advantage of a destructuring technique called *destructured assignment* to save ourselves some keystrokes. In destructured assignment we create a variable with the name of an object’s key that is wrapped in curly braces { } and assign to it the object. Take a look at the example below:

```
const { residence } = vampire; 
console.log(residence); // Prints 'Transylvania'
```

Look back at the `vampire` object’s properties in the first code example. Then, in the example above, we declare a new variable `{ residence }` that extracts the value of the `residence` property of `vampire`. When we log the value of `residence` to the console, `'Transylvania'` is printed.

We can even use destructured assignment to grab nested properties of an object:

```
const { day } = vampire.preferences; 
console.log(day); // Prints 'stay inside'
```
____________________________________________________________________

## Built-In Object Methods

In addition to the object methods that we create ourselves, there are also built in object methods inherent to the JavaScript langauge that we can use on our objects. 

We can use methods such as `.hasOwnProperty()`, `.valueOf()`, `Object.assign()`, `Object.entries()`, and `Object.keys()`. 

- `Object.keys()` method takes an object as the argument and returns an array of all the properties, or keys, that the object has. Note that it *does not* return the value of the key, only the name of the key/property.

- `Object.entries()` method takes an object as the argument and returns each key-value pair as an array that are then nested inside of an array. Example: `[ [key, value], [key, value], [key, value] ]`

- `Object.assign()` method needs at least 2 arguments in order to work, the *target* and the *source(s)*, and the arguments must be given in that order. The source(s) are objects who's properties you want to apply to the target. The target is the object that is receiving the additional properties from the source(s) argument(s), and the target is also what is returned after it has been modified.

Be sure to check the JS documentation for a more comprehensive list and explanation of what each built in object method does.
____________________________________________________________________

# The `<script>` tag

The `<script>` element allows you to add JavaScript code inside an HTML file.

Like most HTML elements, this element has opening and closing tags.

Similar to how `<style>` allows you embed CSS into an HTML file, `<script>` allows you to embed valid JavaScript into an HTML file.

```
<h1>This is an embedded JS example</h1>
<script>
  function Hello() {
    alert ('Hello World');
  }
</script>
```
____________________________________________________________________

## The `src` Attribute

There is a programming concept known as "Separation of Concerns" (SoC).

Instead of having messy code that is all in the same file (having CSS styling and JavaScript scripting inside of the HTML file), web developers separate their code into different files, making each "concern" easier to understand and more convenient to access when changes must be made.

This is the preferable way to handle this kind of stuff. 

Just like when we create a separate `style.css` file to handle the styling of the website and then link it to the HTML file, we create a javascript file and then link that to the HTML file to create advanced functionality within our website. 

We do this with the `src` attribute, which we use to specify the javascript file location.

```
<script src="./exampleScript.js"></script>
```

This would look for a file called **exampleScript.js** that is in the same folder/directory as our **index.html** file. Remember that we can also link external paths (as opposed to this one, which is a relative path).
____________________________________________________________________

## How Are Scripts Loaded?

Browsers use *HTML parsers* which allows the browser to render the elements of an HTML file accordingly. By default, the HTML elements - including `<script>` - are parsed in the order they appear in the HTML file.

When a parser encounters a `<script>` element, it loads the script and then executes its contents before parsing the rest of the HTML. The two main takeaways from this are:

- The parser **DOES NOT** process the next element in the HTML file until it loads and executes the `<script>` element, thus leading to a delay in load time and resulting in a poor user experience.

- Scripts are loaded sequentially, so if on script depends on another script they should be placed in that order inside the HTML file.

## `defer` Attribute

Because the default behavior is the parse each element before moving on to the next element, this can result in slow load times.

We can use the `defer` attribute to specify that a script should only be executed after the HTML file is completely parsed. When the parser encounters a `<script>` element with the `defer` attribute, it loads the script but *defers* the actual execution of the JavaScript until *after* it finishes parsing the rest of the elements of the HTML file.

When is this useful? When a script contains funcitonality that requires interaction with the DOM.

## `async` Attribute

The `async` attribute loads and executes the script asynchornously with the rest of the webpage, meaning that the parser will continue to parse thru the HTML file while the script is being downloaded and executed.

This is useful for scripts that are *independent* of other scripts in order to function accordingly. Meaning if it does not matter exactly at which point the script file is executed, `async` is the most suitable attribute as it optimizes web page loading time.
____________________________________________________________________

## Summary

- HTML creates the skeleton of a webpage, but JavaScript introduces interactivity

- The `<script>` element has an opening and closing tag. You can embed JavaScript code inbetween the opening and closing `<script>` tags.

- You link to external JavaScript files with the src attribute in the opening `<script>` tag.

- By default, scripts are loaded and executed as soon as the HTML parser encounters them in the HTML file, the HTML parser waits to load the entire script before from proceeding to parse the rest of the page elements.

- The `defer` attribute ensures that the entire HTML file has been parsed before the script is executed.

- The `async` attribute will allow the HTML parser to continue parsing as the script is being downloaded, but will execute immediately after it has been downloaded

The old convention was to put scripts right before the `</body>` tag to prevent the script from blocking the rest of the HTML content. Now, the convention is to put the script tag in the `<head>` element and to use the `defer` and `async` attributes.
____________________________________________________________________

# What is the DOM?

The DOM, or *Document Object Model* is a tree-like **M**odel that organizes a webpage's HTML **D**ocument as an **O**bject. It allows programmers to conceptualize  hierarchy and access the elements on a webpage.

It is implemented by browsers to allow JavaScript to access, modify, and update the structure of an HTML web page in an organized way.

## The DOM as a Tree

The DOM tree follows similar logic to that of a family tree. A family tree is made up of family members and their relationships to the family name. In computer science, we would call each family member a node.

We define a *node* as an intersecting point in a tree that contains data.

In the DOM tree, the top-most node is called the *root node*, and it represents the HTML document. The descendants of the root node are the HTML tags in the document, starting with the `<html>` tag followed by the `<head>` and `<body>` tags and so on.

![visualization of the DOM tree](https://static-assets.codecademy.com/Courses/Learn-JavaScript/DOM/domTreeEx2.svg)

## Parent/Child Relationships in the DOM

If we use the metaphor of a family tree we can define some key terminology in the DOM hierarchy.

A *parent* node is any node that is a direct ancestor of another node while a *child* node is a direct descendant of a parent node.

A parent can be a child of another parent and a child can also be a parent of another child. 

For instance, *you* are the child of your parents but *your parents* are the *children* of *their parents*. *You* may also be the *parent* of your own *child*.

These parent/child relationships are used to describe the relationship in various programming concepts. For instance, if you have a `<div>` nested inside of another `<div>` then they also have a parent/child relationship.
____________________________________________________________________

## Nodes and Elements in the DOM

JavaScript scripts typically interact with the *element* nodes (read: HTML elements like `<p>`) within the DOM but will also occasionally interact with the text/content nodes within those elements.

![element nodes in red & sharp corners. text/content nodes in blue & rounded corners](https://static-assets.codecademy.com/Courses/Learn-JavaScript/DOM/domTreeEx4.svg)
____________________________________________________________________

## Attributes of Element Nodes

The DOM allows us to access a node's attributes, such as `class`, `id`, and inline `style`. In the diagram below, the paragraph element with the `id` of `bio` within the HTML file is highlighted. If we accessed that element node in our script, the DOM would allow us to check their value or tweak and modify each of those attributes.

![DOM with highlighted node & its attributes](https://static-assets.codecademy.com/Courses/Learn-JavaScript/DOM/domTreeEx5.svg)
____________________________________________________________________

## Summary

- The DOM is a structural model of a web page that allows for scripting languages to access that page.
- The system of organization in the DOM mimics the nesting structure of an HTML document.
- Elements nested within another are referred to as the children of that element. The element they are nested within is called the parent element of those elements.
- The DOM also allows access to the attributes of an HTML element such as `style`, `id`, `etc`.
____________________________________________________________________

# The Document Keyword

The DOM has methods and properties that allow us to interact with it through JavaScript.

The `document` object in JavaScript is the door to the DOM structure, it allows us to access the root node of the DOM tree. Before we can access a specific element in the page, first you must access the document structure itself. The `document` object allows scripts to access the children of the DOM as properties.

Think of the `document` object as the `root` node of the DOM.

For example, if we wanted to access the `<body>` element from our script we would type `document.body`. We access the `<body>` element as a property of the `document` object. This would return the body element of that DOM.

Here is a [comprehensive list](https://developer.mozilla.org/en-US/docs/Web/API/Document) of all the `document` properties.
____________________________________________________________________

## Tweaking an Element

When we use the DOM to access an HTML element we have access to all of the element's properties.This gives us the ability to modify the contents of the element as well as its attributes and properties.

We can modify the text inside of a `<p>` element, assign a new background color to a `<div>`, etc. For example, the `.innerHTML` property to allow us access to and set the contents of an element.

```
document.body.innerHTML = 'The cat loves the dog.';
```

With the code above, we reassign the conents of the `<body>` element to be the text `'The cat loves the dog'`

We can also add any valid HTML elements as well. The following code replaces the content of the `<body>` with an `<h2>` element.

```
document.body.innerHTML = '<h2>This is a heading</h2>'; 
```

**Note that when we do this it *replaces* all the content within the `<body>` element, meaning that any pre-existing content, such as divs, images, paragraphs, etc., will no longer be there.**
____________________________________________________________________

## Select and Modify Elements

If we want to select a specific element we can access them with CSS selectors.

CSS selectors are typically used within CSS stylesheets to define which HTML elements will have a ruleset applied to them.

We can use the same CSS selectors to access DOM elements with JavaScript. These can be tag names, a class, or an ID, etc.

By using `.querySelector()` we can specify a CSS selector as a string and the script will return the first element that matches the selector. The following code would return the first paragraph `<p>` in the HTML document

```
document.querySelector('p');
```

There are other targeted methods we can use that select elements based on their class, id, or tag name. For example, if you want to access an element directly by its `id` you can use the method `.getElementById()`

```
document.getElementById('bio').innerHTML = 'The description';
```

In the example above, the element with `id = bio` has been selected and we set the *innerHTML* to the text 'The description'.

It would be as if we had

```
<div id = bio>
   'some text inside'
</div>
```

and then changed it to

```
<div id = bio>
   'The description'
</div>
```

We can also use `.getElementsByClassName()` and `.getElementsByTagName()` to return an *array* of all elements that match the query, instead of just a single element. From there we can use bracket notation to access individual elements of the array.

```
// Set first element of .student class as 'Not yet registered'
document.getElementsByClassName('student')[0].innerHTML = 'Not yet registered';
 
// Set second <li> tag as 'Cedric Diggory'
document.getElementsByTagName('li')[1].innerHTML = 'Cedric Diggory`;
```

In the example above, the first element with the class `student` will be set to "Not yet registered" and the second list item `<li>` will be set to "Cedric Diggory".
____________________________________________________________________

## Style an Element

We can also modify an element's style by using the `.style` property. This changes the *inline style* of that HTML tag.

The syntax follows an `element.style.property` format, with `property` representing a CSS property. For example, the following code initializes a variable `blueElement` and then assigns the value of it by using the `document` object and `querySelector()` method to get the first element with `class = blue` and then modifies the `backgroundColor` property.

```
let blueElement = document.querySelector('.blue');
blueElement.style.backgroundColor = 'blue';
```

Notice that normally, in CSS, we would write `background-color` with a hyphen but in JavaScript we access that same property using camelCasing (backgroundColor).

We could also use *chaining syntax* to accomplish the same thing

```
document.querySelector('.blue').style.backgroundColor = 'blue';
```

The only notable difference is that we don't declare a variable within the javascript when we do this.
____________________________________________________________________

## Traversing the DOM

We know about the parent/child relationships in regards to the nodes of the DOM. Each element has a `.parentNode` and `.children` property. The `.parentNode` returns the parent of the specified element in the DOM hierarchy. 

Remember that the `document` element is the *root node* so its `.parentNode` property will always return `null`. The `children` property returns an array of the specified element's children, if the element does not have any children it will return `null`.

```
<ul id='groceries'>
  <li id='must-have'>Toilet Paper</li>
  <li>Apples</li>
  <li>Chocolate</li>
  <li>Dumplings</li>
</ul>
```
Here we have an unordered list element `<ul>` with four list items `<li>` inside.

```
let parentElement = document.getElementById('must-have').parentNode; // returns <ul> element
let childElements = document.getElementById('groceries').children; // returns an array of <li> elements
```

This script has two variables, `parentElement` and `childElements`. 

We get the parent node of the element with the id `must-have`, and set it as the value of `parentElement`, which would be `<ul id='groceries'>`;

Then, we get the children of the element with the id `groceries`, and set that array as the value of `childElements`.
____________________________________________________________________

## Create and Insert Elements

The `.createElement()` method creates a new element based on the specified tag name passed into it as an argument. However, it does not append it to the document. It creates an empty element with no inner HTML.

```
let paragraph = document.createElement('p');
```

This creates an empty paragraph element and stores it as a variable.

We can then assign values to the properties of the newly created element like how we've done previously with exisiting elements.

```
paragraph.id = 'info'; 
paragraph.innerHTML = 'The text inside the paragraph';
```

In order to add it to the web page we must assign it to be the child of an element that already exists on the DOM. We call this process *appending* and we accomplish this by using the `.appendChild()` method, which adds a child element as the parent elements last child node.

This is similar to the `array.push()` method, which adds an array item to the end of the array. The `.appendChild()` method adds a child to the end of a parent element.

The following code would append the `<p>` element stored in the `paragraph` variable to the document body

```
document.body.appendChild(paragraph);
```
This does not replace the content inside the parent, rather it appends, or *pushes* the new element to the end of the body as the last child of the parent.
____________________________________________________________________

## Remove an Element

We can also remove a specified child from a parent element using `.removeChild()`

```
let paragraph = document.querySelector('p');
document.body.removeChild(paragraph);
```

Here, the first paragraph `<p>` in the document is returned as the value for the `paragraph` variable.

Then we remove that first `<p>` element, which is stored in the `paragraph` variable, from the document body.

If we want to *hide* an element rather than completely delete it, we can use the `.hidden` property to set the property to either `true` or `false`.

```
document.getElementById('sign').hidden = true;
```
____________________________________________________________________

## Add Click Interactivity

We can add interactivity to DOM elements by assigning a funciton to run based on an event. Events can include anything from a click to a user mousing over an element. We will cover more about events further into the notes but for now we will focus on the click event.

The `.onclick` property allows you to assign a function to run on when an element is clicked on.

```
let element = document.querySelector('button');
 
element.onclick = function() { 
  element.style.backgroundColor = 'blue' 
};
```

We can also assign the `.onclick` property to a function by name

```
let element = document.querySelector('button');
 
function turnBlue() {
   element.style.backgroundColor = 'blue';
}
 
element.onclick = turnBlue;
```
____________________________________________________________________

## Summary

- The `document` keyword grants access to the root of the DOM in JavaScript.
- The DOM Interface allows you to select a specific element with CSS selectors by using the `.querySelector()` method.
- You can access an element directly by its ID with the `.getElementById()` method which returns a single element.
- You can access an array of elements with the `.getElementsByClassName()` and `.getElementsByTagName()` methods, then call a single element by referencing its placement in the array.
- The `.innerHTML` and `.style` properties allow you to modify an element by changing its contents or style respectively.
- The `.children` property returns a list of an element’s children and the `.parentNode` property returns the element’s closest connected node in the direction towards the root.
- You can create, append, and remove elements by using the `.createElement()`, `.appendChild()` and `.removeChild()` methods respectively.
- The `.onclick` property can add interactivity to a DOM element based on a click event.
____________________________________________________________________

# Events

What is an event? When you refresh your email inbox, double tap on a post, or scroll through a newsfeed — something cool happens in your browser. These actions are known as events!

Events on the web are user interactions and browser manipulations that you can program to trigger functionality. Some other examples of events are:

- A mouse clicking on a button
- Webpage files loading in the browser
- A user swiping right on an image

When a user does any of the above actions, they cause an event to be *fired* or *triggered*.  Being able to respond to these events makes your website interactive and therefore *dynamic*.
____________________________________________________________________

## "Firing" Events

After an event fires on an element in the DOM, an *event handler* funciton can be created to run as a response.

There are three parts to events, the trigger, the listener, and the handler. Think of it like a dog doing a trick.

When you give a command, like "speak", we are *triggering an event*. The dog hears the command, this is analogous to an *event listener*. Then the dog performs the command, in this case it would bark, and this would be like the *event handler*. 

Most events in the browser take place without being noticed — the events are undetected because there is no event handler associated with the event to execute an action. Event handlers are crucial for creating interactive websites with JavaScript.
____________________________________________________________________

## Event Handler Registration

Using the `.addEventListener()` method we can have a DOM element listen for a specific event and execute a block of code when the event is detected.

The DOM element that listens for an event is called the *event target* and the block of code that runs when the event happens is called the *event handler*.

```
let eventTarget = document.getElementById('targetElement');
 
eventTarget.addEventListener('click', function() {
  // this block of code will run when click event happens on eventTarget element
});
```
In the above example:

- We initalize a variable "eventTarget" and set its value using the DOM method `.getElementByID`.
- Then we use the `.addEventListener()` method on `eventTarget`. This takes two arguments:
	1. An event name in *string* format
	2. An event handler function
- In this example, we used the 'click' event, which fires when the user clicks on the  `eventTarget` element
- Then the code block in the event handler function will execute when the `click` event is detected.

In this example, we used an anonymous function as the event handler. However, it is best practice to create a named event handler function. Your code will remain organized and reusable this way.

```
function eventHandlerFunction() {
  // this block of code will run when click event happens
}
 
eventTarget.addEventListener('click', eventHandlerFunction);
```

Here, the named function `eventHandlerFunction` is passed as the second argument of the `.addEventListener` method instead of defining an anonymous function within the method.
____________________________________________________________________

## Adding Event Handlers

Event handlers can also be registered by setting an `.onevent` property on a DOM element (event target).

The pattern for registering a specific event is to append an element with `.on` followed by the lowercased event type name. For instance, if we want to register a click event with this pattern we would write:

```
eventTarget.onclick = eventHandlerFunction;
```

Its important to know that using the `.onevent` property and `.addEventListener()` will both register event listeners. However, with `.onevent` it allows only one event handler function to be attached to the event target as opposed to the `.addEventListener()` method which can have multiple event handler functions.

Both are widely used so it is important to know how to use both.
____________________________________________________________________

## Removing Event Handlers

The `.removeEventListener()` method is used to reverse the `.addEventListener()` method; this takes two arguments:

1. The event type as a string
2. The event handler function

```
eventTarget.removeEventListener('click', eventHandlerFunction);
```

Because there can be multiple event handler functions associated with a particular event, `.removeEventListener()` needs bot the exact event type name and the name of the event handler function you want to remove. 

If `.addEventListener()` was provided an anonymous function, then that event listener **cannot** be removed.
____________________________________________________________________

## Event Object Properties


JavaScript stores events as [event objects](https://developer.mozilla.org/en-US/docs/Web/API/Event) with their related data and functionalities as properties and methods. When an event is triggered, the event object can be passed as an argument to the event handler function.

```
function eventHandlerFunction(event){
   console.log(event.timeStamp);
}
 
eventTarget.addEventListener('click', eventHandlerFunction);
```
In the example above, when the `'click'` event is triggered on the `eventTarget`, the `eventHandlerFunction` receives `event`, the Event object, which has information related to the `'click'` event. Then, we log the time it took for the event to be triggered since the document was loaded by accessing the `.timeStamp` property of the `event` object.

There are pre-determined properties associated with event objects. You can call these properties to see information about the event, for example:

- `.target`to reference the element that the event is registered to
- `.type` to access the name of the event
- `.timeStamp` to access the number of milliseconds that passed since the document loaded and the event was triggered
____________________________________________________________________

## Event Types

Most events in the DOM take place without being noticed because there are no event handlers connected to them.

Also, some registered events don't depend on user interaction to fire. For instance, the `load` event fires after website files completely load in the browser.

You can read the [MDN Events Reference](https://developer.mozilla.org/en-US/docs/Web/Events) page to see all the events available.
____________________________________________________________________

## Mouse Events

When you use a mouse device on a website, *mouse events* fire. For instance, `click` is a common mouse event.

There is also

- `wheel` which fires when the mouse wheel is scrolled/rotated while the mouse is over the event target.

- `mousedown` is similar to `click` but fires when the mouse button goes down. It does not require the mouse button to be released to fire.

- `mouseup` is the reverse of `mousedown`, it only fires when the mouse button is released.

- `mouseover` is fired when the mouse enters the content of an element

- `mouseout` is fired when the mouse leaves an element.
____________________________________________________________________

## Keyboard Events

Another common type of events are keyboard events which are triggered by user interaction with keyboard keys in the browser.

- `keydown` is fired when a user presses a key down; similar to `mousedown`.
- `keyup` is fired when a user releases a key; similar to `mouseup`
- `keypress` is fired when a user presses a key down and releases it; this is similar to 'click'

Keyboard events have unique properties assigned to their event objects like the `.key` property that stores the value of the key pressed by the user. You can program the event handler function to react to a specific key or react to any interaction with the keyboard.
____________________________________________________________________

## Summary

- You can register events to DOM elements using the `addEventListener()` method.
- The `addEventListener()` method takes two arguments: an event type and an event handler function.
- When an event is triggered on the event target, the registered event handler function executes.
- Event handler functions can also be registered as values of `onevent` properties of their event target.
- Event object properties like `.target`, `.type`, and `.timeStamp` are used to provide information about the event.
- The `addEventListener()` method can be used to add multiple event handler functions to a single event.
- The `removeEventListener()` method stops specific event handlers from “listening” for specific events firing.
____________________________________________________________________

## Intro to Handlebars

The external library, Handlebars.js, provides developers with a templating engine that allows you to generate reusable HTML using Javascript. Another benefit is that Handlebars keeps a clear separation of when you're writing HTML or JavaScript.

Invitations are a great real life example of a template - they usually include the invitees name, the venue location, the time and date, and maybe a short description.

If you had to create multiple cards from scratch you would realize that a lot of the information is repeated - the only change you would really need to make is the name.

Creating a template with a blank space for the name would make it much easier for you to invite everyone.

An example of templating in regards to web development would be something your "my profile" or "my account" page on social media. It has the same material for every person and really the only big differences would be their profile picture/icon and their username.

You wouldn't want to create a unique page for every single visitor, you'd use a template and sub in the values you need to.
____________________________________________________________________

## Implementing Handlebars

*Boilerplate code* refers to sections of code that you can use with little to no modification.

Whenever we use a library, like Handlebars, we might end up using code that is specific to that library. 

To use a library we must first link it within our HTML file using the `<script>` tag within our `<head>` element. We can use the source attribute, `src`, to link the CDN (Content Delivery Network).

```<script src="cdn.link.goes.here"></script>```

Then we also need to include another `<script>` tag with a unique `id` and `type` attributes.

```<script id="ice-cream" type="text/x-handlebars-template">
	!<-- scripted content goes here -->
</script>

```

Then in our JavaScript file, we need to get the HTML stored in the Handlebars script

```const source = document.getElementById('ice-cream').innerHTML;```

Then we use `Handlebars.compile()` to return a templating function

```const template = Handlebars.compile(source);```

Then we create an object that handles all the contextual information that we would want to sub in to our template

```
const context = {
	flavor: 'vanilla';
};
```

Then we pass in the `context` object to the templating function to get a compiled template

```const compiledHTML = template(context);```

And then finally we render the compiled template onto the web page

```
const iceCreamText = document.getElementById('scream');
iceCreamText.innerHTML = compiledHtml;
```
____________________________________________________________________

## Using Handlebars expressions

The power of Handlebars lies in its reusability and extensibility. *Handlebars expressions* allow us to accomplish this.

Inside a script, Handlebar expressions are wrapped with double braces, `{{` `}}`. The content inside the curly braces serves as a placeholder.

For example, if we use the script

```
<script id="foo" type="text/x-handlebars-template">
  <p>{{bar}}</p>
</script>
```

And our JS file looks like 

```
const source = document.getElementById('foo').innerHTML;
 
const template = Handlebars.compile(source);
 
const context = {
  bar: 'Text of the paragraph element'
};
 
const compiledHtml = template(context);
```

After we run the code, the expression ``{{bar}}`` is replaced with the value of `context.bar` in our JS file, which would be `<p> Text of the paragraph element </p>`
____________________________________________________________________

## Handlebars "If" block helper

We can check for a specific object property before we insert a value using the `{{if}}` helper block. It's similar to the `if` conditional in JS but there is a different syntax

```
<script id="ifHelper" type="text/x-handlebars-template">
    {{#if argument}}
      // Code to include if the provided argument is truthy 
    {{/if}}
</script>
```
Notice that the example above has both an opening and closing expression. The code block between those expressions will be added to the final HTML if the `argument` provided is truthy.
____________________________________________________________________

## Handlebars "Else" section

What if your `{{if}}` block helper argument is falsy? We can add a default line of code by creating an *else section* using Handlebar's `{{else}}` expression.

```
{{#if argument}}
  // Code to include if the provided argument is truthy 
{{else}}
  // Code to include if the provided argument is falsy 
{{/if}}
```
____________________________________________________________________

## Handlebars "Each"

The `{{each}}` block allows you to interate through an array. There is an opening `{{#each}} expression and a closing `{{/each}}` expression. Inside each block, `{{this}}` acts as a placeholder for the element in the iteration.

```
{{#each someArray}}
  <p>{{this}} is the current element!</p>
{{/each}}
```
Which we would pair with an array like so:

```
const context = {
  someArray: ['First', 'Second', 'Third'] 
}
```

Which after compiling the HTML would look like

```
<p>First is the current element!</p>
<p>Second is the current element!</p>
<p>Third is the current element!</p>
```

Using `{{this}}` also gives you access to the properties of the element being iterated over.

For instance, if we were using the following array inside the `context` object

```
const context = {
  someArray: [
    {shape: 'Triangle'},
    {shape: 'Circle'},
    {shape: 'Square'}
  ] 
}
```

And our template looked like this

```
{{#each someArray}}
  <p>The current shape is: {{this.shape}}!</p>
{{/each}}
```
After going through the steps of compiling, the finished HTML will look like

```
<p>The current shape is: Triangle!</p>
<p>The current shape is: Circle!</p>
<p>The current shape is: Square!</p>
```
____________________________________________________________________

## Combining "If" and "Each"

We can combine `{{if}}` and `{{each}}` to create more dynamic expressions.

Assume we have our context object as so:

```
const context = {
  languages: [
    {
      name: 'HTML',
      modern: true
    },
    {
      name:'CSS',
      modern: true
    }, 
    {
      name: 'JavaScript',
      modern: true
    },
    {
      name: 'COBOL',
      modern: false
    }
  ]
};
```
It contains a languages array, which holds multiple objects with the keys `name` and `modern`

```
<script id="languagesTemp" type="text/x-handlebars-template">
      {{#each languages}}
      	<div class="card">
          {{#if this.modern}}
            <p>I should learn {{this.name}}.</p>
          {{else}}
            <p>When I have time, I'll learn {{this.name}}.</p>
          {{/if}}
        </div>
      {{/each}}
    </script>
```

In this example above, we iterate through the languages array and for each element in the array we add a div with a paragraph element that says "I should learn (language)" *IF* the language has their `modern` property set to true. If the `modern` property is set to false, we add a div with a different paragraph element.
____________________________________________________________________

## Summary

- Handlebars is an external library used to create templates which are a mix of HTML, text, and expressions.
- Handlebars uses expressions which are wrapped inside double braces like: `{{someVariable}}`
- A script tag with a type of `"text/x-handlebars-template"` is used to deliver a template to the browser.
- Handlebar.compile() returns a templating function from a template script intended for Handlebars.
- A template created from `.compile()` will take an object as an argument and use it as context to generate a string containing HTML.
- Handlebars has built in block helpers which can be included in a Handlebars script.
- Block helpers have a starting expression and an ending expression. The starting expression will have a `#` appears before a keyword. The ending expression will have the same keyword but with a `/` character to denote the end.
- The `{{if}}` will conditionally render a block of code.
- An `{{else}}` expression can be inserted into an if helper block and used as part of the conditional statement.
- `{{each}}` is another built-in helper expression which accepts an array to iterate through.
- In the block helper functions, the `{{this}}` expression gives context and serves as a placeholder for the current value.
____________________________________________________________________

# Classes

JavaScript is an *object-oriented programming* language, or OOP, that we can use to model real-world items.

Classes are a tool that we can use to quickly produce similar objects.

Imagine we have a dog object with properties like name, breed, behavior, etc. Instead of creating multiple individual dog objects, we can create a Dog *class* that serves as a template for creating new Dog objects which we can then assign their own names, breeds, behaviors, etc.

This is a great way to reduce duplcate code and debugging time.
____________________________________________________________________

## Constructor

Although there are similarities between class and object syntax, there is one important method that sets them apart: the *constructor* method.

JS calls the `constructor()` method every time it creates a new *instance* of a class.

```
class Dog {
  constructor(name) {
    this.name = name;
    this.behavior = 0;
  }
}
```
- `Dog` is the name of our class. By convention, we capitalize and CamelCase class names
- JavaScript will invoke the `constructor()` method every time we create a new instance of our `Dog` class
- This `constructor()` method can accept arguments. In this case, it accepts one argument: `name`.
- Inside of the `constructor()` method, we use the `this` keyword. In the context of a class, `this` refers to an instance of that class. In the `Dog` class, we use `this` to set the value of the Dog instance's `name' property to the `name` argument.
- On the line under `this.name`, we create a property called `behavior`, which will keep track of the number of times a dog misbehaves. The `behavior` property is always initialized to zero.
____________________________________________________________________

## Instance

An *instance* is an object that contains the property names and methods of a class but qith unique property values.

```
class Dog {
  constructor(name) {
    this.name = name;
    this.behavior = 0;
  } 
}
 
const halley = new Dog('Halley'); // Create new Dog instance
console.log(halley.name); // Log the name value saved to halley
// Output: 'Halley'
```

In the above example, we use the `new` keyword to create an instance of our `Dog` class.

- We create a new variable named `halley` that will store an instance of our `Dog` class.
- Using the `new` keyword, we generate a new instance of the `Dog` class, this calls the `constructor()` method and runs the code inside of it, then returns the new instance.
- When we use `Halley` as the argument of the `Dog` constructor it sets the `name` property to `Halley`
____________________________________________________________________

## Methods

We can add methods and getters to our classes just like an object. The syntax is the same **except you can not include commas between methods.**

```
class Dog {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
 
  get name() {
    return this._name;
  }
 
  get behavior() {
    return this._behavior;
  }
 
  incrementBehavior() {
    this._behavior++;
  }
}
```
In the above example, we add getter methods for `name` and `behavior`. Notice that we also prepended the property names with underscores (`_name` and `_behavior`), which indicates that these properties should not be accessed directly.

Under the getters, we add a method named `.incrementBehavior()`, which when called on a Dog instance, it adds `1` to the `_behavior` property.

Note that between each method we **did not** include commas.
____________________________________________________________________

## Method Calls

The syntax for calling methods and getters on an instance is the same as calling them on an object - append the instance with a period, then the property or the method name. 

For methods you must also include opening and closing parentheses.

```
let nikko = new Dog('Nikko'); // Create dog named Nikko
nikko.incrementBehavior(); // Add 1 to nikko instance's behavior
let bradford = new Dog('Bradford'); // Create dog name Bradford
console.log(nikko.behavior); // Logs 1 to the console
console.log(bradford.behavior); // Logs 0 to the console
```

In the above example we create two new `Dog` instances, `nikko` and `bradford`. We incremented the behavior of our `nikko` isntance but not `bradford`, so when we access `nikko.behavior` it returns `1` and if we access `bradford.behavior` it returns `0`.
____________________________________________________________________

## Inheritance

When multiple classes share properties or methods, they become candidates for *inheritance* - a tool developers use to decrease the amount of code they need to write.

With inheritance, you can create a *parent* class (also known as a superclass) with properties and methods that multiple *child* classes (also known as subclasses) share.

The child classes inherit the properties and methods from their parent class.

Previously, we used a class `Dog` for our examples. If we wanted to also create a `Cat` class that had similar properties like `name` and `behavior` but also have unique properties like `usesLitterbox`, we can create a parent class `Animal` and then make `Dog` and `Cat` as subclasses.

![Visualization of inheritance from superclasses to subclasses](https://cdn.discordapp.com/attachments/513823285188886532/1052914404926177320/image.png)

```
class Animal {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
 
  get name() {
    return this._name;
  }
 
  get behavior() {
    return this._behavior;
  }   
 
  incrementBehavior() {
    this._behavior++;
  }
} 
```
When we have the parent class defined, we can then *extend* those shared properties and methods to the subclasses.

```
class Cat extends Animal {
  constructor(name, usesLitter) {
    super(name);
    this._usesLitter = usesLitter;
  }
}
```

- The `extends` keyword makes the *methods* and *properties* of the animal class available inside the cat class.
- The `super` keyword calls the constructor of the parent class. In this case, `super(name)` passes the name argument of the `Cat` class to the constructor of the `Animal` class. When the `Animal` constructor runs, it sets `this._name = name;` for new `Cat` instances.
- We have a new property `_usesLitter` that is unique to the `Cat` class, so we set it in the `Cat` constructor.
____________________________________________________________________

## Static Methods

Sometimes you will want a class to have methods that aren’t available in individual instances, but that you can call directly from the class.

Take the `Date` class, for example - you can both create `Date` instances to represent whatever date you want or you can call *static* methods, like `Date.now()` which returns the current date, directly from the class.

The `.now()` method is static, so you can call it directly from the class, but not from an instance of the class.

```
class Animal {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }
 
  static generateName() {
    const names = ['Angel', 'Spike', 'Buffy', 'Willow', 'Tara'];
    const randomNumber = Math.floor(Math.random()*5);
    return names[randomNumber];
  }
} 
```
In the example above we create a `static` method called `.generateName()` that returns a random name when its called. Because of the `static` keyword we can only access this method by appending it to the `Animal` class.

```
console.log(Animal.generateName()); // returns a name
```

The example above would return a name however the example below *would not* because you cannot call a static method on an instance

```
const tyson = new Animal('Tyson'); 
tyson.generateName(); // TypeError
```
____________________________________________________________________

## Summary

- Classes are templates for objects.
- Javascript calls a *constructor* method when we create a new instance of a class.
- *Inheritance* is when we create a parent class with properties and methods that we can extend to child classes.
- We use the `extends` keyword to create a subclass.
- The `super` keyword calls the `constructor()` of a parent class.
- Static methods are called on the class, but not on instances of the class.
____________________________________________________________________

# Modules

## What is a Runtime Environment?

A runtime environment is where your program will be executed. It determines what global objects your program can access and it can also impact how it runs. This article covers the two JavaScript runtime environments:

1. the runtime environment of a browser, like Chrome or Firefox
2. the Node runtime environment
____________________________________________________________________

### A Browser's Runtime Environment

The most common place where JS code is executed is in a browser. For example, we can use a text editor like VS Code, create an HTML file and then open that HTML file with our browser. For example:

```
<!-- my_website.html -->
<html>
  <body>
    <h1> My Website </h1>
    <script> window.alert('Hello World'); </script>
  </body>
</html>
```

When we load this website, the embedded script will execute and the `window.alert()` method will create a pop-up box in your browser with the text `"Hello World"`. 

How is this possible? Where does the `window.alert()` method come from and how can it control your browser?

The answer, is that you are executing this code in the *browser's runtime environment*. The `window.alert()` method is built into this environment and any program executed in a browser has access to this method. The `window` object provides access to a huge amount of data and functionality relating to the open browser beyond just `.alert()`.

Applications created for and executed in the browser are known as *front-end* applications. For a long time, JavaScript code would *only* be executed in a browser and was used exclusively for creating front-end applications.
____________________________________________________________________

### The Node Runtime Environment

In 2009, the Node *runtime environment* was created for the purpose of executing JavaScript code *without* a browser, thus enabling programmers to create *full-stack* applications using only the JavaScript language.

Node is an entirely different runtime environment, meaning that browser environment data values and functions, like `windows.alert()`, can not be used. Instead, the Node runtime environment gives back-end applications access to a variety of features unavailable in a browser, such as access to the server's file system, database, and network.

For example, suppose we created a file named **my-app.js**. We can check to see the directory that the file is located in using the Node runtime environment variable `process`.

```
// my-app.js
console.log(process.env.PWD);
```
- `process` is an object containing data relating to the JavaScript file being executed.
- `process.env` is an object containing environment variables such as `process.env.PWD` which contains the current working directory (**P**ring **W**orking **D**irectory).

In order to execute the Javascript code in this file, we need to be sure that we have set up Node on our computer. We can download the most current version of Node LTS [here](https://nodejs.org/en/).

After its been downloaded and installed, open a new terminal window and run the command `which node` to print the filepath to Node and/or run the command `node -v` to print the current version that is installed.

We could then use the command `node my-app.js` which tells your computer to execute the `my-app.js` file in the Node environment. 

We can lso use the `node` command without a file argument to open up the Node Read-Eval-Print-Loop (REPL)
____________________________________________________________________

### Summary

A *runtime environment* is where your program will be executed. JavaScript may be executed in one of two runtime environments:
1. A browser's runtime environment
2. The Node runtime environment

In each of these environemnts, different data values and functions are available and these differences help distinguish front-end applications from back-end applications.

- Front-end JS applications are executed in a browser's runtime environment and have access to the `window` object.
- Back-end JS applications are executed in the Node runtime environment and have access to the file system, databases, and networks attached to the server.
____________________________________________________________________

## What are Modules?

Modules are reusable pieces of code in a file that can be exported and then imported for use in another file. A *modular* program is one whos components can be separated, used individually, and recombined to create a complex system.

Consider the diagram below:

![digram of modules that create a JS program/app](https://static-assets.codecademy.com/Courses/Learn-JavaScript/Modules/modular-program-diagram.svg)

*The words 'module' and 'file' are often used interchangably.*

Instead of having the entire program written within **my_app.js**, its components are broken up into separate modules that each handle a particular task. For example, the **database_logic.js** module may contain code for storing and retrieving data from a database while the **date_formatting.js** module may contain functions designed to easily convert date values from one format to another.

This modular strategy is sometimes called *separation of concerns* and is useful for several reasons, such as:

- finding, fixing, and debugging code made more easy
- reuse and recycle defined logic in different parts of your application
- keep information private and protected from other modules
- prevent pollution of the global namespace and potential naming collisions, by cautiously selecting variables and behavior we load into a program.

Implementing modules in your program requires a small bit of management. We need to know how to:

- Use Node.js `module.exports` object to *export* code from a file - meaning its functions and/or data can be used by other files/modules.
- Use Node.js `require()` function to *import* functions and/or data from another module.

- Use the ES6 `export` statement to *export* code from a file
- Use the ES6 `import` statement to *import* functions and/or data from another module.
____________________________________________________________________

## Implementation of Modules: Node.js vs ES6

There are multiple ways of implementing modules depending on the runtime environment in which your code is executed. In JavaScript, there are two runtime environments and each has a preferred module implementation:

- The Node runtime environment and the `module.exports` and `require()` syntax
- The browser's runtime environment and the ES6 `import`/`export` syntax.
____________________________________________________________________

## Implementing Modules in Node

Every JavaScript file that runs in a Node environment is treated as a distinct module. The functions and data defined within each module can be used by any other module, as long as those resources are properly *exported* and *imported*.

Suppose you wanted to write a simple program that would display the freezing point and boiling point of water in Fahrenheit. However, you only know the values in Celsius to be 0 (freezing) and 100 (boiling). Luckily you happen to know how to convert Celsius to Fahrenheit!

```
/* water-limits.js */
function celsiusToFahrenheit(celsius) {
  return celsius * (9/5) + 32;
}
 
const freezingPointC = 0;
const boilingPointC = 100;
 
const freezingPointF = celsiusToFahrenheit(freezingPointC);
const boilingPointF = celsiusToFahrenheit(boilingPointC);
 
console.log(`The freezing point of water in Fahrenheit is ${freezingPointF}`);
console.log(`The boiling point of water in Fahrenheit is ${boilingPointF}`);
```
Executing this file using Node would look something like this:

```
$ node water-limits.js
The freezing point of water in Fahrenheit is 32
The boiling point of water in Fahrenheit is 212
```
Now, you decide to write a second program. In this program, the user can input any temperature value in Celsius and the program responds by printing the input temperature converted to Fahrenheit.

For example, you might want to be able to run such a program and see a response like so:

```
$ node celsius-to-fahrenheit.js 100
100 degrees Celsius = 212 degrees Fahrenheit
```

The JavaScript below would do just that:

```
/* celsius-to-fahrenheit.js */
function celsiusToFahrenheit(celsius) {
    return celsius * (9/5) + 32;
}
 
const celsiusInput = process.argv[2]; // Get the 3rd input from the argument list
const fahrenheitValue = celsiusToFahrenheit(celsiusInput);
 
console.log(`${celsiusInput} degrees Celsius = ${fahrenheitValue} degrees Fahrenheit`);
```

Notice that our variable `celsiusInput` is assigned the value of `process.argv[2]`. When a program is executed in the Node environment, `process.argv` is an array holding the arguments provided. 

Two code snippets above, we see the line `node celsius-to-fahrenheit.js 100`. This means that `process.argv` would be an array that looks like ['node', 'celsius-to-fahrenheit.js', '100'], therefore `process.argv[2]` would return `100`.

Additionally, both **celsius-to-fahrenheit.js** and **water-limits.js** implement the function `celsiusToFahrenheit()`. Since we wrote this function twice, if for whatever reason we ever need to make changes to the function, we will have to make those changes in both modules.

To solve this issue, we can create a module that exports a `celsiusToFahrenheit()` function that can be used by both of these programs.
____________________________________________________________________

### `module.exports`

To create a new module, simply create a new file where the functions can be declared. Then, to make these functions available to other files, add them as properties to the built-in `module.exports` object.

```
/* converters.js */
function celsiusToFahrenheit(celsius) {
  return celsius * (9/5) + 32;
}
 
module.exports.celsiusToFahrenheit = celsiusToFahrenheit;
 
module.exports.fahrenheitToCelsius = function(fahrenheit) {
  return (fahrenheit - 32) * (5/9);
};
```
The above code snippet demonstrates two ways of exporting functions from a module.

- First, the function `celsiusToFahrenheit()` is declared.
- On the next line, the first method of exporting a function is shown. We use the `module.exports` object and append it with the name of what we want our exported function name to be, `.celsiusToFahrenheit` and then assign it the value of the declared function within the module **converters.js**, which is also named `celsiusToFahrenheit`.
- On the line below, we demonstrate an alternative method for exporting a function from a module. We declare and assign a new function expression to `module.exports.fahrenheitToCelsius`. This new method is designed to convert F back to C.
- Both of these approaches successfully store a function within the `module.exports` object.

`module.exports` is an object that is built-in to the Node.js runtime environment. Now, other files can import this object and make use of these two functions with another feature that is built-in to the Node.js runtime environment: the `require()` function.
____________________________________________________________________

### `require()`

The `require()` function accepts a string as an argument. The string provides the **file path** to the module you would like to import.

We can update our **water-limits.js** file and use `require()` to import the methods within the `module.exports` object.

```
/* water-limits.js */
const converters = require('./converters.js');
 
const freezingPointC = 0;
const boilingPointC = 100;
 
const freezingPointF = converters.celsiusToFahrenheit(freezingPointC);
const boilingPointF = converters.celsiusToFahrenheit(boilingPointC);
 
console.log(`The freezing point of water in Fahrenheit is ${freezingPointF}`);
console.log(`The boiling point of water in Fahrenheit is ${boilingPointF}`);
```

In this example, `./` is the relative path indicating that **converters.js** is stored in the same folder as **water-limits.js**. When you use `require()`, the entire `module.exports` object is returned and stored in the variable `converters`. We can now access both the `.celsiusToFahrenheit()` and `.fahrenheitToCelsius()` methods in our **water-limits.js** module.
____________________________________________________________________

### Using Object Destructuring to be more Selective With `require()`

In many cases, modules will export a large number of functions but only one or two of them are needed. You can use object destructuring to extract only the needed functions.

Let's *only* extract the `.celsiusToFahrenheit()` method

```
/* celsius-to-fahrenheit.js */
const { celsiusToFahrenheit } = require('./converters.js');
 
const celsiusInput = process.argv[2]; 
const fahrenheitValue = celsiusToFahrenheit(celsiusInput);
 
console.log(`${celsiusInput} degrees Celsius = ${fahrenheitValue} degrees Fahrenheit`);
```

With this approach, the remainder of the program works the same way but the program avoids importing a function it does not need.
____________________________________________________________________

## Implementing Modules using ES6 Syntax

In the early days of web development, JavaScript usage was fairly minimal - a script here to add some interactivity to a page and a script there to automate away some simple task.

Nowadays, however, JavaScript dominates the web and scripts have ballooned into large and cumbersome behemoths. The average size of a website, in terms of kilobytes of JavaScript data transferred, has grown over 5 times from 2010 to 2020.

This is not meant to be overwhelming but rather to show that web applications drive much of modern society and are far more capable than could have been imagined when the World Wide Web was created in 1989. 

This growth makes a clear need for modularity as the capabilities and size of these scripts grow.

In 2015, the syntax for natively implementing modules was created with the release of ES6 (ECMAScript 6). Since then, it has been adopted by most modern browsers and is the de facto approach for implementing modular applications in the browser.
____________________________________________________________________

### Implementing Modules in the Browser

Suppose you wanted to build a simple web app with some hidden text that is revealed when a button is pressed

![.gif of a JavaScript app that reveals text when a button is pressed](https://static-assets.codecademy.com/Courses/Learn-JavaScript/Modules/ESModules-Secret-Messages.gif)

To create this website, you could create two files, **secret-messages.html** and **secret-messages.js**, and then store them together in a folder called **secret-messages**.

```
secret-messages/
|-- secret-messages.html
|-- secret-messages.js
```
Lets take a look at the HTML file first:

```
<!-- secret-messages.html --> 
<html>
  <head>
    <title>Secret Messages</title>
  </head>
  <body>
    <button id="secret-button"> Press me... if you dare </button>
    <p id="secret-p" style="display: none"> Modules are fancy! </p>
    <script src="./secret-messages.js"> </script>
  </body>
</html>
```
- The **secret-messages.html** page renders a button element and a hidden paragraph element
- Then it loads the script **secret-messages.js**using the file path `"./secret-messages.js"`. Remember that the `./` before the file name indicates that the file being referenced (secret-messages.js) is in the same folder as the file referencing it(secret-messages.html).

Lets take a look at the JavaScript file:

```
/* secret-messages.js */
const buttonElement = document.getElementById('secret-button');
const pElement = document.getElementById('secret-p');
 
const toggleHiddenElement = (domElement) => {
    if (domElement.style.display === 'none') {
      domElement.style.display = 'block';
    } else {
      domElement.style.display = 'none';
    }
}
 
buttonElement.addEventListener('click', () => {
  toggleHiddenElement(pElement);
});
```
- We create DOM objects to reference the element and paragraph elements which are stored in `buttonElement` and `pElement`, respectively.
- We declare the function `toggleHiddenElement()` which has the parameter called 'domElement'. We can use both `buttonElement` or `pElement` as the argument for the function.
- We then add an event listener to `buttonElement` which listens for the `click` event and responds by calling the `toggleHiddenElement()` with `pElement` as the argument.

Now, suppose you wanted to create a second webpage with similar features. There is still a button, but this time clicking it reveals an image. Using similar logic as the program above, this can be achieved with the following file structure:

```
secret-image/
|-- secret-image.html
|-- secret-image.js
```
The HTML might look like this:

```
<!-- secret-image.html --> 
<html>
  <head>
    <title>Secret Image</title>
  </head>
  <body>
    <button id="secret-button"> Want to see something cool? </button>
    <img id="secret-img" src="imageURL.jpg" style="display: none">
    <script src="./secret-image.js"> </script>
  </body>
</html>
```
… and the JavaScript might look like this:

```
/* secret-image.js */
const buttonElement = document.getElementById('secret-button');
const imgElement = document.getElementById('secret-img');
 
const toggleHiddenElement = (domElement) => {
    if (domElement.style.display === 'none') {
      domElement.style.display = 'block';
    } else {
      domElement.style.display = 'none';
    }
}
 
buttonElement.addEventListener('click', () => {
  toggleHiddenElement(imgElement);
});
```
Given that much of the code in these two programs are similar, creating this second website was fairly straightforward. In particular, notice that the `toggleHiddenElement()` function is copied line for line from **secret-messages.js**

Just like our previous examples in the **Implementing Modules in Node** section, this can lead to maintenance issues in the future as we would need to update both functions if anything ever needed to be fixed or changed.

Instead, we should create a single function within a single module, then export it from that module and import it into the other modules that that need it.

With this approach, only one function would ever need to be maintained. Furthermore, additional functions could be exported by the module and used by both programs, further reducing repetition.
____________________________________________________________________

### ES6 Named Export Syntax

A module must be entirely contained within a file. So, let’s first consider where a new module may be placed within the file system. Since it needs to be used by both of these projects, you may want to put it in a mutually accessible location. The entire file structure containing both projects and this new module, let’s call it dom-functions.js, could look like this:

```
secret-image/
|-- secret-image.html
|-- secret-image.js
secret-messages/
|-- secret-messages.html
|-- secret-messages.js
modules/
|-- dom-functions.js    <-- new module file
```
Inside dom-functions.js, the functions you wish to reuse can be exported using the *named export* syntax below:

```export { resourceToExportA, resourceToExportB, ...}```

Using this syntax, the name of each exported resource is listed between curly braces and separated by commas. Below, you can see how this is implemented in the new module file dom-functions.js:

```
/* dom-functions.js */
const toggleHiddenElement = (domElement) => {
    if (domElement.style.display === 'none') {
      domElement.style.display = 'block';
    } else {
      domElement.style.display = 'none';
    }
}
 
const changeToFunkyColor = (domElement) => {
  const r = Math.random() * 255;
  const g = Math.random() * 255;
  const b = Math.random() * 255;
 
  domElement.style.background = `rgb(${r}, ${g}, ${b})`;
}
 
export { toggleHiddenElement, changeToFunkyColor };
```
- The functions `toggleHiddenElement()` and `changeToFunkyColor()` are declared. They both accept a `domElement` as their arguments and will hide/show the element or set the background color to a random color, respectively.
- Then we export the functions using the ES6 `export` statement and are now available to be imported and used by other files.

> If you want to try this out on your own computer, you will need to spin up a local server or else you will run into [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) issues. [Check out this article](https://www.codecademy.com/articles/spinning-up-a-local-server) on creating a local server with VSCode and the Live Server extension.

In addition to the syntax above, in which all named exports are listed together, individual values may be exported *in-line* as named exports by simply placing the `export` keyword in front of the variable’s declaration. Here is the same example using this syntax:

```
/* dom-functions.js */
export const toggleHiddenElement = (domElement) => {
  // logic omitted...
}
 
export const changeToFunkyColor = (domElement) => {
  // logic omitted...
}
```
____________________________________________________________________

### ES6 Import Syntax

The ES6 syntax for importing named resources from modules is similar to the export syntax:

```import { exportedResourceA, exportedResourceB } from '/path/to/module.js';```

Let’s update the **secret-messages** program such that it now imports functionality from **dom-functions.js**. Doing so requires two important steps. First, update **secret-messages.js**:

```
/* secret-messages.js */
import { toggleHiddenElement, changeToFunkyColor } from '../modules/dom-functions.js';
 
const buttonElement = document.getElementById('secret-button');
const pElement = document.getElementById('secret-p');
 
buttonElement.addEventListener('click', () => {
  toggleHiddenElement(pElement);
  changeToFunkyColor(buttonElement);
});
```
- The functions `toggleHiddenElement()` and `changeToFunkyColor()` are imported from the module **dom-functions.js**, using the path `../modules/dom-functions.js`. The `../` indicates that the **modules/** folder is in the same folder as the parent folder **secret-messages/**.
- When the button is clicked, the now imported function `toggleHiddenElement()` is called with the `pElement` as an argument.
- In addition, `changeToFunkyColor()` is also called with the `buttonElement` as an argument.

Now, we must also update **secret-messages.html**:

```
<!-- secret-messages.html --> 
<html>
  <head>
    <title>Secret Messages</title>
  </head>
  <body>
    <button id="secret-button"> Press me... if you dare </button>
    <p id="secret-p" style="display: none"> Modules are fancy! </p>
    <script type="module" src="./secret-messages.js"> </script>
  </body>
</html>
```
The changes here are subtle - the only thing that changes is the addition of the attribute `type='module'` to the `<script>` element. Failure to do so can cause some browsers to throw an error.

Those are the basics to exporting and importing using the ES6 `export` and `import` syntax!
____________________________________________________________________

### Renaming Imports to Avoid Naming Collisions

Inevitably, you will run into a situation where the resources you wish to import share a name with some other value that already exists in your program (or from another imported module).

For example, suppose you had access to two modules, greeterEspanol.js and greeterFrancais.js. Each exports a function called greet():

```
/* inside greeterEspanol.js */
const greet = () => {
  console.log('hola');
}
export { greet };
 
/* inside greeterFrancais.js */
const greet = () => {
  console.log('bonjour');
}
export { greet };
```

Now, let’s say you wanted to use each of these functions in a program, called main.js, that simulates a conversation between a spanish-speaker and a french-speaker.

```
import { greet } from 'greeterEspanol.js';
import { greet } from 'greeterFrancais.js';
```

The code above will throw an error on line 2 due to the fact that the identifier greet has already been defined on line 1. Thankfully, ES6 includes syntax for renaming imported resources by adding in the keyword `as`. It looks like this:

```
import { exportedResource as newlyNamedResource } from '/path/to/module'
```

Let’s see how this could work within main.js

```
/* main.js */
import { greet as greetEspanol } from 'greeterEspanol.js';
import { greet as greetFrancais } from 'greeterFrancais.js';

greetEspanol(); // Prints: hola
greetFrancais(); // Prints: bonjour
```

Now, both of the imported functions can be called within main.js using their new identifiers, `greetEspanol()` and `greetFrancais()`.
____________________________________________________________________

### Default Exports and Imports

Previously, we have been exporting a module's resources individually by name. There is also an option to export a single value to represent the entire module called the *default export*. Often, though not always, the default export value is an object containing the entire set of functions and/or data values of a module.

The syntax for exporting a default object looks like this:

```
const resources = { 
  valueA, 
  valueB 
}
export { resources as default };
```

With this syntax, the object containing the module’s resources is first declared and then is exported on the next line. At first glance, it looks like the `resources` object is being exported as a named export. However, the clause `as default` renames the exported object to `default`, a reserved identifier that can only be given to a single exported value.

You may also see this shorthand syntax where the value follows `export default` is the default value to be exported:

```
const resources = {
  valueA,
  valueB
}
export default resources;
```
____________________________________________________________________

### Importing Default Values

The syntax for importing default exports looks like this:

```import importedResources from 'module.js';```

Notice that the curly braces are gone from the import statement. This syntax is actually shorthand for `import { default as importedResources } from 'module.js'` and the imported `default` value may be given any name the programmer chooses.

It should be noted that if the `default` export is an object, the values inside cannot be extracted until after the object is imported, like so:

```
// This will work...
import resources from 'module.js'
const { valueA, valueB } = resources;
 
// This will not work...
import { valueA, valueB } from 'module.js'
```
Let’s return to the prior example. The dom-functions.js module from above could be rewritten to use default exports like so:

```
/* dom-functions.js */
const toggleHiddenElement = (domElement) => {
    if (domElement.style.display === 'none') {
      domElement.style.display = 'block';
    } else {
      domElement.style.display = 'none';
    }
}
 
const changeToFunkyColor = (domElement) => {
  const r = Math.random() * 255;
  const g = Math.random() * 255;
  const b = Math.random() * 255;
 
  domElement.style.background = `rgb(${r}, ${g}, ${b})`;
}
 
const resources = { 
  toggleHiddenElement, 
  changeToFunkyColor
}
export default resources;
```

This default exports object can now be used within secret-messages.js like so:

```
import domFunctions from '../modules/dom-functions.js';
 
const { toggleHiddenElement, changeToFunkyColor } = domFunctions;
 
const buttonElement = document.getElementById('secret-button');
const pElement = document.getElementById('secret-p');
 
buttonElement.addEventListener('click', () => {
  toggleHiddenElement(pElement);
  changeToFunkyColor(buttonElement);
});
```

Notice how toggleHiddenElement() and changeToFunkyColor() are now methods of the imported object called domFunctions and are extracted using ES6 destructuring syntax! It should be noted that the identifier domFunctions can be chosen as the programmer sees fit. If you recall, the syntax used in the snippet above is shorthand for:

```import { default as domFunctions } from '../modules/dom-functions.js';```
____________________________________________________________________

# Errors & Error Handling

It is inevitable that at some point in your coding process you will encounter bugs. It's important to understand how to debug these errors and that you won't always know the solution right away.

Typically, errors are shown in red text. Usually, red signifies things like "STOP! DANGER! DO NOT ENTER!" but in programming we should not carry over this kind of mindset. Although red text does signify a bug/error, it is something that can be resolved and should not be a deterrent.

As your code increases in complexity, the number of errors you'll encounter rises at a similar rate. An error means that you're trying to something that might be complicated, and it doesn't quite work yet, but that doesn't mean you should stop trying!

In fact there are entire engeineering roles built around finding and fixing errors and almost all major technology companies offer cash rewards to intrepid programmers who can find bugs in their software.

Encounter bugs is one of the best ways to improve your code. Bugs show you where the weaknesses are, what you want your code to accomplish, and guide you towards building more reliable and secure products.
____________________________________________________________________

## Tools to Tackle Code Errors
____________________________________________________________________

### 1. Dissect The Error

A lot of the time when you are presented an error message there will be tons of boilerplate details that aren't important to the actual error. We should find the part of the error code that designates what line the berror is happening on, typically it is at the top of the error message.

```
TypeError: students.filter is not a function
    at /home/runner/FearlessNewDev/index.js:21:26
```

Usually, it will designate the line and the character at which the error occurs, something like 21:26 tells us that the error occurs on line 21, character 26.
____________________________________________________________________

### 2. Ask Yourself, Is the Solution In The Error?

Often, you'll encounter syntax errors that show you exactly where the error occured and what the error was. For example, consider the error below:

```
/home/runner/FearlessNewDev/index.js:1
for (let x = 0; x < 10, x++) {
                                       ^

SyntaxError: Unexpected token ')'
```
In this case, the compiler is pointing to the syntax issue with the `^` symbol which sometimes makes it easier to debug. However, the real issue is that there is an accidental comma after `x < 10` instead of a semicolon. Error messages can help, but you will still need to use your developer knowledge to fix the error.
____________________________________________________________________

### 3. Search on the Web for Instances of This Error

Sometimes step 2 will not apply and you will have to dive a little deeper into the error. You can copy and paste the important part of the error message into a serach engine and look through the results until you find someone else who has also run into that issue. To get better search results, you can include relevant keywords and modify the error message to be more generic.

In step 1, we have the error message `TypeError: students.filter is not a function`. Its highly unlikely that someone else is using the `filter()` method on a `students` variable, so instead of copy/pasting the error message as is we can edit it to make a more generic search query. Something like "TypeError: object filter() is not a function" and then adding the language in your search query as well can have much better results.

From there, you will probably find that the `filter()` method will only work for arrays. You can then consult the documentation for more in-depth details on how the method works and how to use it properly.
____________________________________________________________________

### 4. Compare Different Use Cases to Yours

Often you will not find someone who was trying to do the exact same thing you were trying to do, but who still encountered the same error. Read through their code a bit and see if it is comparable to yours. Even if their code is wildly different, the one or two lines that threw the error might be very similar to your code, so the solution may end up being the same
____________________________________________________________________

### 5. Try To Implement The Solution

You can then tweak the code you find online to match your use case and then test it out. Worst case scenario is that you dont resolve the error and you have to try again. Best case is that it's fixed and you learned what was causing the error!

Every solution you implement is a new tool you can add to your programmer’s toolbox, and another error you will know how to solve in the future.
____________________________________________________________________

### 6. If It Doesn't Work, Repeat Steps 2-4

If you don't find your solution, keep searching through Google and Stack Overflow - the answer will be there! Consult the documentation and refine your search queries until you find the information that you need. This is part of being a developer and a skill that you will grow along with your actual programming skills.

### 7. Ask The Question Yourself

Okay so... maybe the answer *isn't* out there. Yet. There is a wealth of information and resources on the web but you might be the first one doing something completely new and shiny. If that's the case, ask for help! Use websites like Stack Overflow to ask questions and try to supply as much information and relevant code snippets that will enable others to provide feedback and hopefully a solution to your issues.
____________________________________________________________________

# Debugging JavaScript Code
____________________________________________________________________

## Error Stack Traces

When a compiler comes across a piece of code that can't be interpreted, it throws an error back to you. This information is logged as an **error stack trace** - a printed message containing information about where the error occured, what type of error was thrown, and a description of the error.

```
/home/ccuser/workspace/learn-javascript-debugging-code/app.js:1
myVariable;
^
 
ReferenceError: myVariable is not defined
...
```
Here we can see the the error occured in `app.js` on line 1. We can see that the type of error was a `ReferenceError` and that the error message is that `myVariable is not defined`.
____________________________________________________________________

## JavaScript Error Types

Three common error types include:

- **SyntaxError**: This occurs when a typo creates invalid code and cannot be interpreted by the compiler. When you see this, scan your code to make sure you have all the proper opening/closing brackets, braces, parentheses and that you didn't include any invalid commas or semicolons.
- **ReferenceError**: This occurs if you try to use a variable that does not exist or a variable that is out of scope. Check to see if all your variables are properly declared.
- **TypeError**: This occurs when you attempt to perform an operation on a value of the wrong type. For example, trying to use the `.push()` array method on a string.

There are seven types of built-in JavaScript errors in total and you can find more information in the [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error).
____________________________________________________________________

## Debugging Errors Process

1. Run your code. Using the first error’s stack trace, identify the error’s type, description, and location.
2. Go to the file name and line number indicated by the error stack trace. Using the error type and description, identify the bug in your code.
3. Fix the bug and re-run your code.
4. Repeat steps 1-3 until your code no longer throws any errors.
____________________________________________________________________

## Locating Silent Bugs

Errors thrown by the computer are really useful because they identify the bug type and location for you right away. However, even if your code runs error-free, it is not necessarily bug-free.

You may find that your code is consistently returning incorrect values without throwing any errors. A lack of thrown errors does not mean your code logic is completely correct.

An incredibly powerful tool for locating bugs is a method you likely learned very early on in your JavaScript journey: `console.log()`!

By adding print statements to our code, we can identify where things have gone wrong.
____________________________________________________________________

## Summary

1. **Is Your Code Throwing Errors?** If so, read the *error stack trace* to get the location of the error, the type of error, and the description of the error.

2. **Is your code broken but not throwing errors?** As in, does your code technically "work" but are the return values not what you are expecting? If so, walk through your code using `console.log()` statements to find where these unexpected results are occuring, isolate the bug and fix it.

3. **Did you locate teh bug using steps 1 and 2, but still can't fix the bug?** Consult documentation to make sure you're using the methods and functions properly. If you are still stuck, trying Googling your issue and consult Stack Overflow for help. Read through previous solutions or post your own Stack Overflow question if none exist on the topic.
____________________________________________________________________

# Error Handling

This is the process of programmatically anticipating and addressing errors. In JavaScript, we handle errors using the keywords `try` and `catch`. 

Sometimes, we’ve written code that successfully returns a value but a different value from what we expected. Our program continues running, and we might not even realize anything went wrong until much later. It’s like making soup and accidentally adding sugar instead of salt. In the end we still have soup, but it might not be soup that we want to eat. We will not be focusing on these mistakes.

But what if we tried to move our soup to the table but dropped it because it was too hot? Then our soup-making process is over— there would be no soup. We can’t always stop errors before they occur, but we can include a backup plan in our program to anticipate and respond to the errors to ensure that our program continues running.

We 'try' to move the soup to the table, making sure that there's someone or something nearby to `catch` the soup in case we drop it.
____________________________________________________________________

## Runtime Errors

Error messages contain useful information that tell us why our program isn't working, or why the error was *thrown*. When an error is thrown, the program stops running and the console displays an error message in red text.

When we execute code and a line of code throws an error, that error is referred to as a *runtime error*. In JS, there are built-in error objects that have a `name` and `message` property which tell us what went wrong. Examples of these are `ReferenceError` and `TypeError`, which we briefly touched on in the previous section above.

```
const reminder = 'Reduce, Reuse, Recycle';
reminder = 'Save the world';
// TypeError: Assignment to constant variable.
console.log('This will never be printed!');
```
In the example above, when we try to reassign a constant variable, the `TypeError` is thrown. Code that is written *after* a thrown runtime error will not be evaluated, so the `console.log()` statement will not run.
____________________________________________________________________

## Constructing an Error

We can create our own error messages, separate from Javascript's built-in errors, that we can use to inform us about any mistakes that are being made when the code is being ran.

For example, what if we need to let a user know that the string passed as an argument to a function does not meet some kind of requirement? For example, like when you try to create a new password and it's not long enough or strong enough of a password.

We can use the built in `Error` function to make our own error object with a unique message.

The `Error` function takes an argument of a string which becomes the value of the error's `message` property.

```
console.log(Error('Your password is too weak.'));
// Prints: Error: Your password is too weak.
```
You might also see errors created with the `new` keyword. Both methods lead to the same functionality.

```
console.log(new Error('Your password is too weak.'));
// Prints: Error: Your password is too weak.
```
Keep in mind that creating an error is not the same as throwing an error. A thrown error will cause the program to stop running. We will cover how to throw our created errors in the next section.
____________________________________________________________________

## The `throw` Keyword

Creating an error doesn’t cause our program to stop — remember, an error must be thrown for it to halt the program.

To throw an error in JavaScript, we use the `throw` keyword like so:

```
throw Error('Something wrong happened');
// Error: Something wrong happened
```

When we use the `throw` keyword the error is thrown and the code afterwards will not execute, just like a built-in JavaScript error. For example:

```
throw Error('Something wrong happened');
// Error: Something wrong happened
 
console.log('This will never run');
```
____________________________________________________________________

## The `try...catch` Statement

Thrown errors cause our program to stop running, however, we have the ability to anticipate and *handle* these errors by writing code to address the error and **allow our program to continue running**.

In JS, we use `try...catch` statements to anticipate and handle errors. Take a look at the example below:

```
try {
  throw Error('This error will get caught');
} catch (e) {
  console.log(e);
}
// Prints: This error will get caught
 
console.log('The thrown error that was caught in the try...catch statement!');
// Prints: 'The thrown error that was caught in the try...catch statement!'
```
- We have code that follows `try` inside curly braces known as the `try` block
- Inside the `try` block we insert code that we anticipate might throw an error
- Since we want to see what happens *if* an error is thrown in the try block, we *intentionally* throw an error with the message 'This error will get caught'.
- Following the `try` block is the `catch` statement which acepts the thrown error from the `try` block. `e` represents the thrown error.
- The curly braces that follow `catch(e)` is known as the *catch block* and contains code that executes to handle the error.
- In this case, since the error was caught, our `console.log()` statement *after* the `try...catch` statement prints.

Generally speaking, in a `try...catch` statement, we evaluate code in the `try` block and if the code throws an error then the code inside the `catch` block will handle the error for us.

The provided example above is just meant to showcase *how* a `try...catch` statement works.
____________________________________________________________________

## Handling with `try...catch`

In the previous exercise we caught an error that we intentionally threw, but we also can use a `try...catch` statement to handle built-in errors that are thrown by the Javascript engine that is reading and evaluating our code.

```
const someVar = 'Cannot be reassigned';
try {
  someVar = 'Still going to try';
} catch(e) {
  console.log(e);
}
// Prints: TypeError: Assignment to constant variable.
```

In the example above, we **did not** use the `throw` keyword to throw a custom error, rather we tried to re-assign a `const` variable and a `TypeError` was thrown.

Then in our `catch` block, we logged the error to the console.

Using a `try...catch` statement for built-in JavaScript errors is really beneficial when we need to use data from an external source that’s not written directly in our program.

Let’s say we expect to grab an array from a database but the information we get back is a string. In our program, we could have a function that only works on arrays. If that function was called with a string instead of an array we would get an error and our program would stop running!

However, we can use a `try...catch` statement to handle the thrown error for us which allows our program to continue running and we receive a message knowing what went wrong! 
____________________________________________________________________

# JavaScript Promises

In programming, an *asynchronous operation* is one that allows a computer to "move on" to other tasks while waiting for the asynchronous operation to complete. This means that time-consuming operations don't have to bring everything else in our program to a halt.

Consider the real world example of cleaning your house which involves asynchronous operations like using a dishwasher or washing our clothes. While the dishes or clothes are being washed in the machine, you are free to do other chores around the house.

Similarly, web development makes use of asynchronous operations. Operations like making a network request or querying a database can be time-consuming, but JavaScript allows us to execute other tasks while awaiting their completion

JavaScript allows us to handle asynchronicity using the `Promise` object introduced with ES6.
____________________________________________________________________

## What is a Promise?

Promises are objects that represent the eventual outcome of an asynchronous operation.

A `Promise` object can be in one of three states:

- **Pending**: The initial state. The operation has not completed yet.
- **Fulfilled**: The operation has completed successfully and the promise now has a *resolved value*. For example, a request's promise might resolve with a JSON object as its value.
- **Rejected**: The operation has failed and hte promise has a reason for the failer. The reason is usually an `Error` of some kind.

When a promise is fulfilled or rejected it, we refer to it as *settled*, as in no-longer pending. Using our previous real world example of using a dishwasher lets consider the potential states:

- **Pending** The dishwasher is running but has not completed the washing cycle
- **Fulfilled** The dishwasher has completed the cycle and the dishes are clean
- **Rejected** The dishwasher encountered a problem (it did not have any soap!) and returns unclean dishes.

If our dishwashing promise is fulfilled, we’ll be able to perform related tasks, such as unloading the clean dishes from the dishwasher. If it’s rejected, we can take alternate steps, such as running it again with soap or washing the dishes by hand.

All promises eventually settle, enabling us to write logic for what to do if the promise fulfills or if it rejects.
____________________________________________________________________

## Constructing a Promise Object

To create a new `Promise` object we need to use the `new` keyword and the `Promise` constructor method.

```
const executorFunction = (resolve, reject) => { };
const myFirstPromise = new Promise(executorFunction);
```

The `Promise` constructor method takes a function parameter called the *executor function* that runs atuomatically when the constructor is called. The executor function generally starts an asynchronous operation and dictates how the promise should be settled.

The executor function has two function parameters, usually referred to as the `resolve()` and `reject()` functions. These function parameters **are not** defined by the programmer. 

When the `Promise` constructor runs, JavaScript will pass **its own** `resolve()` and `reject()` functions into the executor function.

- `resolve` has one argument. Under the hood, if invoked, `resolve()` will change the promise's status from `pending` to `fulfilled`, and the promise's resolved value will be set to the argument passed into `resolve()`

- `reject` is a function that takes a reason or error as an argument. Under the hood, if invoked, `reject()` will change the promise's status from `pending` to `rejected` and the promise's rejection reason will be set to the argument passed into `reject()`.

For example:

```
const executorFunction = (resolve, reject) => {
  if (someCondition) {
      resolve('I resolved!');
  } else {
      reject('I rejected!'); 
  }
}
const myFirstPromise = new Promise(executorFunction);
```

- We have the `executorFunction()` which has two function parameters: `resolve` and `reject`
- If `someCondition` evaluates to `true`, we invoke `resolve()` with the argument string `I resolved!`. 
- If not, we invoke `reject()` with the argument string `I rejected!`
- Then we declare the variable `myFirstPromise` and assign its value as a `Promise` object, using the constructor method `new Promise()`
- We pass `executorFunction()` in as the argument for the `new Promise()` constructor method.

In our example, `myFirstPromise` resolves or rejects based on a simple condition, but, in practice, promises settle based on results of asynchronous operations.

For example, a database request may fulfill with the data from a query or reject with an error thrown. In this exercise, we’ll construct promises which resolve synchronously to more easily understand how they work.
____________________________________________________________________

## The Node setTimeout() Function

The `setTimeout()` function has 2 parameters, a callback function and a number representing a delay in milliseconds.

```
const delayedHello = () => {
  console.log('Hi! This is an asynchronous greeting!');
};
 
setTimeout(delayedHello, 2000);
```

Here the function `delayedHello` will be invoked after *at least* 2 seconds. Wait, "at least"? Yes because the delay is performed asynchronously - the rest of our program won't stop executing during the delay.

Asynchronous JavaScript uses something called *the event-loop*. After two seconds, `delayedHello()` is added to a line of code waiting to be run. Before it can run, any synchronous code from the program will run. Next, any code in front of it in the line will run. This means it might be more than two seconds before `delayedHello()` is actually executed.
____________________________________________________________________

## Consuming Promises

The initial state of an asynchronous promise is `pending` but we have a guarantee that it will settle.

So, how do we tell the computer what will happen after the promise settles? Promise objects come with a method `.then()`. It allows us to say "I have a promise, when it settles, **then** here's what I want to happen..."

In the case of our dishwasher example:

- If our promise *rejects*, meaning we still have dirty dishes, **then** we have to add soap and run the dishwashers again.
- If our promise *fulfills*, this means we have clean dishes, **then** we need to put the dishes away.

`.then()` is a higher-order function - it takes two callback functions as arguments. We refer to these callbacks as *handlers*. When the promise settles, the appropriate handler will be invoked with that settled value.

- The first handler, sometimes called `onFulfilled`, is a *success handler*, and it should contain the logic for the promise resolving.
- The second handler, sometimes called `onRejected`, is a *failure handler*, and it should contain the logic for the promise rejecting.

We can invoke `.then()` with one, both, or neither handler. This allows for flexibility but it can also make debugging tricky.

If the appropriate handler is not provided, instead of throwing an error, `.then()` will just return a promise with the same settled value as the promise it was called on.

One important feature of `.then()` is that it *always* returns a promise.
____________________________________________________________________

## Success and Failure Callback Functions

To handle a "successful" promise, or a promise that resolved as *fulfilled*, we invoke the `.then()` on the promise and pass in the success handler callback function.

```
const prom = new Promise((resolve, reject) => {
  resolve('Yay!');
});
 
const handleSuccess = (resolvedValue) => {
  console.log(resolvedValue);
};
 
prom.then(handleSuccess); // Prints: 'Yay!'
```
- `prom` is a promise which will resolve to `'Yay!'`.
- We define a function, `handleSuccess()`, which prints the argument passed to it.
- We invoke `prom‘s` `.then()` function passing in our `handleSuccess()` function.
- Since `prom` resolves, `handleSuccess()` is invoked with `prom`‘s resolved value, `'Yay'`, so `'Yay'` is logged to the console.

This is a extremely simply example meant to showcase how these success/fail handle
callback functions.

With typical promise consumption, we won't know whether a promise will resolve or reject, so we'll need to provide the logic for either case. We can pass both a success callback and a failure callback to `.then()`.

```
let prom = new Promise((resolve, reject) => {
  let num = Math.random();
  if (num < .5 ){
    resolve('Yay!');
  } else {
    reject('Ohhh noooo!');
  }
});
 
const handleSuccess = (resolvedValue) => {
  console.log(resolvedValue);
};
 
const handleFailure = (rejectionReason) => {
  console.log(rejectionReason);
};
 
prom.then(handleSuccess, handleFailure);
```
In this example, we declare `prom` which is a promise object that will randomly resolve `yay!` or reject with `ohhh noooo!`

We pass two handler functions to `.then()`. The first will be invoked with `yay!` if the promise resolves, the second will be invoked with `ohhh nooo!` if the promise rejects.

> Remember: The success callback is sometimes called the “success handler function” or the onFulfilled function. The failure callback is sometimes called the “failure handler function” or the onRejected function
____________________________________________________________________

## Using `catch()` with Promises

One way to write cleaner code is to follow a principle called *separation of concerns*. Separation of concerns means organizing code into distinct sections each handling a specific task. It enables us to quickly navigate our code and know where to look if something isn’t working.

Remember, `.then()` will return a promise with the same settled value as the promise it was called on if no appropriate handler was provided. This implementation allows us to separate our resolved logic from our rejected logic. Instead of passing both handlers into one `.then()`, we can chain a second `.then()` with a failure handler to a first `.then()` with a success handler and both cases will be handled.

```
prom
  .then((resolvedValue) => {
    console.log(resolvedValue);
  })
  .then(null, (rejectionReason) => {
    console.log(rejectionReason);
  });
```
Since JavaScript doesn’t mind whitespace, we follow a common convention of putting each part of this chain on a new line to make it easier to read. To create even more readable code, we can use a different promise function: `.catch()`.

The `.catch()` function takes only one argument, `onRejected`. In the case of a rejected promise, this failure handler will be invoked with the reason for rejection. Using `.catch()` accomplishes the same thing as using a `.then()` with only a failure handler.

Let’s look at an example using `.catch()`:

```
prom
  .then((resolvedValue) => {
    console.log(resolvedValue);
  })
  .catch((rejectionReason) => {
    console.log(rejectionReason);
  });
```

- `prom` is a promise which randomly either resolves with `'Yay!'` or rejects with `'Ohhh noooo!'`.
- We pass a success handler to `.then()` and a failure handler to `.catch()`.
- If the promise resolves, `.then()`‘s success handler will be invoked with `'Yay!'`.
- If the promise rejects, `.then()` will return a promise with the same rejection reason as the original promise and `.catch()`‘s failure handler will be invoked with that rejection reason.
____________________________________________________________________

## Chaining Multiple Promises

A common pattern we'll see with asynchronous programming is multiple operations which depend on each other to execute or that must be executed in a certain order.

We might make one request to a database and use the data returned to use to make another request and so on! We can illustrate that with another cleaning example, washing clothes:

We take our dirty clothes and put them in the washing machine. If the clothes are cleaned, **then** we'll want to put them in the dryer. After the dryer runs, if the clothes are dry, **then** we can fold them and put them away.

This process of chaining promises together is called *composition*. Promises are designed with composition in mind! Here's a very simple example:

```
promiseFunctionA ()
    .then ((resolveValueA) => {
        return promiseFunctionB(resolveValueA);
})
    .then ((resolveValueB) => {
        console.log(resolveValueB);
});
```
- We invoke a function `promiseFunctionA` which returns a promise object
- We invoke `.then()` with an anonymous function as the success handler
- Inside the success handler, we **return** a new promise. This new, second promise, is the result of invoking the function `promiseFunctionB` with the first promise's resolved value as its argument.
- We invoke a second `.then()` to handle the logic of the second promise settling.
- Inside that second `.then()` we have an anonymous function as the success handler, which logs the second promise's resolved value to the console.

In order for our chain to work properly, we had to `return` the promise `functionPromiseB(resolveValueA)`.

This ensured that the return value of the first `.then()` was our second promise, instead of the default return of a new promise with the same settled value as the initial.
____________________________________________________________________

## Avoiding Common Mistakes

Promise composition allows for much more readable code than the nested callback syntax that preceeded it. 

However, it can still be easy to make mistakes and we will cover two common mistakes with promise compositions below:

**Mistake 1:** Nesting promises instead of chaining them

```
returnsFirstPromise()
.then((firstResolveVal) => {
  return returnsSecondValue(firstResolveVal)
    .then((secondResolveVal) => {
      console.log(secondResolveVal);
    })
})
```
Here you can see that the first `.then()` returns a new promise, however, our following `.then()` is still nested inside of the first `.then()`'s anonymous function body.

**Mistake 2:** Forgetting to `return` a promise

```
returnsFirstPromise()
.then((firstResolveVal) => {
  returnsSecondValue(firstResolveVal)
})
.then((someVal) => {
  console.log(someVal);
})
```
Here, everything is in its proper place (i.e. the second `.then()` is **not** nested inside of the first `.then()`) however there is no `return` keyword in the first `.then()`. 

Since forgetting to return our promise won't throw an error, this can be really tricky to debug.
____________________________________________________________________

## Using Promise.all()

When done correctly, promise composition is a great way to handle situations where asynchronous operations depend on each other or execution order matters. What if we’re dealing with multiple promises, but we don’t care about the order? Let’s think in terms of cleaning again.

For us to consider our house clean, we need our clothes to dry, our trash bins emptied, and the dishwasher to run. We need **all* of these tasks to complete but not in any particular order. Furthermore, since they’re all getting done asynchronously, they should really all be happening at the same time!

To maximize efficiency we should use *concurrency*, multiple asynchronous operations happening together. With promises, we can do this with the function `Promise.all()`.

`Promise.all()` accepts an array of promises as its argument and returns a single promise. That single promise will settle in one of two ways:

- If every promise in the argument array resolves, the single promise returned from `Promise.all()` will resolve with an array containing the resolve value from each promise in the argument array.
- If any promise from the argument array rejects, the single promise returned from `Promise.all()` will immediately reject with the reason that promise rejected. This behavior is sometimes referred to as *failing fast*.

Let’s look at a code example:

```
let myPromises = Promise.all([returnsPromOne(), returnsPromTwo(), returnsPromThree()]);
 
myPromises
  .then((arrayOfValues) => {
    console.log(arrayOfValues);
  })
  .catch((rejectionReason) => {
    console.log(rejectionReason);
  });
```
Let’s break down what’s happening:

- We declare `myPromises` assigned to invoking `Promise.all()`.
- We invoke `Promise.all()` with an array of three promises— the returned values from functions.
- We invoke `then()` with a success handler which will print the array of resolved values if each promise resolves successfully.
- We invoke `.catch()` with a failure handler which will print the first rejection message if any promise rejects.
____________________________________________________________________

## Summary

- Promises are JavaScript objects that represent the eventual result of an asynchronous operation.
- Promises can be in one of three states: pending, resolved, or rejected.
- A promise is settled if it is either resolved or rejected.
- We construct a promise by using the `new` keyword and passing an executor function to the `Promise` constructor method.
- `setTimeout()` is a Node function which delays the execution of a callback function using the event-loop.
- We use `.then()` with a success handler callback containing the logic for what should happen if a promise resolves.
- We use `.catch()` with a failure handler callback containing the logic for what should happen if a promise rejects.
- Promise composition enables us to write complex, asynchronous code that’s still readable. We do this by chaining multiple `.then()`‘s and `.catch()`‘s.
- To use promise composition correctly, we have to remember to `return` promises constructed within a `.then()`.
- We should chain multiple promises rather than nesting them.
- To take advantage of concurrency, we can use `Promise.all()`.
____________________________________________________________________

# Async Await

ES8 provides a new syntax for handling asynchronous action `async...await`. This syntax allows us to write asynchronous code that reads similarly to traditional synchronous, imperative programs.

The `async...await` syntax does not introduce new functionality into the language, but rather it introduces a new syntax for using promises and generators. Both of these were already built into the language. Despite this, `async...await` powerfully improves the readability and scalability of our code.
____________________________________________________________________

## The `async` Keyword

The `async` keyword is used to write functions that handle asynchronous actions. We wrap our asynchronous logic inside a function prepended with the `async` keyword, then we invoke that function.

```
async function myFunc() {
  // Function body here
};
 
myFunc();
```
We can also create `async` function expressions

```
const myFunc = async () => {
  // Function body here
};
 
myFunc();
```

`async` functions always return a promise. This means we can use traditional promise syntax, like `.then()` and `.catch` with our `async` functions. An `async` function will return one of three ways.

- If there's nothing returned from the function, it will return a promise with a resolved value of `undefined`.
- If there's a non-promise value returned from the function, it will return a promise resolved to that value.
- If a promise is returned from the function, it will simply return that promise.

```
async function fivePromise() { 
  return 5;
}
 
fivePromise()
.then(resolvedValue => {
    console.log(resolvedValue);
  })  // Prints 5
```
In the example above, even though we return `5` inside the function body, what’s actually returned when we invoke `fivePromise()` is a promise with a resolved value of `5`.
____________________________________________________________________

## The `await` operator

`async` functions are almost always used with the additional keyword `await` inside the function body.

The `await` keyword can only be used inside an `async` function.

`await` is an operator that returns the resolved value of a promise. Since promises resolve in an indeterminate amount of time, `await` halts/pauses the execution of our `async` function until a given promise is resolved.

In most situations, we're dealing with promises that were returned from functions. 

We can `await` the resolution of the promise being returned inside an `async` function.

```
async function asyncFuncExample(){
  let resolvedValue = await myPromise();
  console.log(resolvedValue);
}
 
asyncFuncExample(); // Prints: I am resolved now!
```

In this example:
- We create the asynchronous function `asyncFuncExample()`.
- Within the function body of `asyncFuncExample`:
	- We run the function `myPromise()` - which for the sake of this example was imported from a library - prepended by the `await` keyword. 
	-This tells the computer to **not** run the rest of the `asyncFuncExample` body until `myPromise` has finished running and returned a resolve value.
- Once the `myPromise()` function has finished executing it stores the returned resolve value in a local variable `resolvedValue`.
- Then `resolvedValue` is printed to the console.

We are able to handle the logic for a promise in a way that reads like synchronous code.
____________________________________________________________________

## Writing async Functions

We cannot forget the `await` keyword when writing `async` functions. It may seem obvious but this can be a tricky mistake to catch because the function will still run - it just won't have the desired results.

Lets take the follow code as an example. The code snippet below is a promise function that resolves after 1second with the resolve value of 'Yay, I resolved!'.

```
let myPromise = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('Yay, I resolved!')
    }, 1000);
  });
}
```

Now, we'll write two `async` functions - one that includes the `await` keyword and one that does not.

```
async function noAwait() {
 let value = myPromise();
 console.log(value);
}
 
async function yesAwait() {
 let value = await myPromise();
 console.log(value);
}
 
noAwait(); // Prints: Promise { <pending> }
yesAwait(); // Prints: Yay, I resolved!
```

The function `noAwait` does not include the `await` keyword and because of that, the function body is not paused and the `value` variable was assigned the promise object itself since the `myPromise()` function had not resolved yet.

The function `yesAwait` **does** include the `await` keyword and because of that, the function body **did** pause and the `value` variable was assigned the returned resolve value  of `myPromise()`.
____________________________________________________________________

## Handling Dependent Promises

The true beauty of `async...await` is when we have a series of asynchronous actions which depend on one another. For example, we might make a network request based on a query to a database.

In that case, we would need to *wait* to make the network request until we had the results from the database.

With native promise syntax, we use a chain of `.then()` functions making sure to return each one correctly:

```
function nativePromiseVersion() {
  returnsFirstPromise()
    .then((firstValue) => {
      console.log(firstValue);
      return returnsSecondPromise(firstValue);
    })
   .then((secondValue) => {
      console.log(secondValue);
    });
}
```
In the example above:

- We have a function `nativePromiseVersion()` which runs `returnsFirstPromise` on the first line.
- When `returnsFirstPromise` is settled, we invoke `.then()`, which takes the resolved value of `returnsFirstPromise` as an argument, `firstValue`.
- `firstValue` is logged to the console
- Next, we return the value of `returnsSecondPromise()` with `firstValue` as its argument
- When `returnsSecondPromise` has settled, we take the resolved value as the argument for another `.then()` method as `secondValue` 
- Finally, `secondValue` is logged to the console

However, we can create the same functionality using `async...await`

```
async function asyncAwaitVersion() {
  let firstValue = await returnsFirstPromise();
  console.log(firstValue);
  let secondValue = await returnsSecondPromise(firstValue);
  console.log(secondValue);
}
```
- We have a function `asyncAwaitVersion()` which runs the function `returnsFirstPromise` prepended by the `await` keyword.
- When `returnsFirstPromise()` is finished executing, the settled value is stored in the `firstValue` variable.
- We log `firstValue` to the console.
- Next, we run `returnsSecondPromise` as an `await` function, using `firstValue` as the argument.
- When `returnsSecondPromise` has settled, that settled value is stored in `secondValue`
- `secondValue` is then logged to the console.

The `async...await` syntax can save us some typing but the length reduction isn't the main point.

Given these two versions of functionality (native promise vs. async...await), the `async...await` version more closely resembles synchronous code, which helps developers maintain and debug their code.

The `async...await` syntax also makes it easy to store and refer to resolved values from promises further back in our chain, which is a much more difficult task with native promise syntax.
____________________________________________________________________

## Handling Errors

When we use `.catch()` in a long promise chain, there is no indication of where in the chain the error was thrown. This can make debugging challenging.

With `async...await`, we can use `try...catch` statements for error handling. By using this syntax, we can handle errors in the same way we do with synchronous code but we can also catch asynchronous errors as well. This makes debugging easier!

```
async function usingTryCatch() {
 try {
   let resolveValue = await asyncFunction('thing that will fail');
   let secondValue = await secondAsyncFunction(resolveValue);
 } catch (err) {
   // Catches any errors in the try block
   console.log(err);
 }
}
 
usingTryCatch();
```

Since `async` functions return promises we can still use a native promise's `.catch()` with an `async` function.

```
async function usingPromiseCatch() {
   let resolveValue = await asyncFunction('thing that will fail');
}
 
let rejectedPromise = usingPromiseCatch();
rejectedPromise.catch((rejectValue) => {
console.log(rejectValue);
})
```
Sometimes, this is used in the global scope to catch final errors in complex code.
____________________________________________________________________

## Handling Independent Promises

What if our `async` function contains multiple promises **which are not dependent on the results of one another to execute**?

```
async function waiting() {
 const firstValue = await firstAsyncThing();
 const secondValue = await secondAsyncThing();
 console.log(firstValue, secondValue);
}
 
async function concurrent() {
 const firstPromise = firstAsyncThing();
 const secondPromise = secondAsyncThing();
console.log(await firstPromise, await secondPromise);
}
```

In the `waiting()` function, we pause our function until our first promise is resolved and then move on to the second promise. Once the second promise resolved, we print both the values to the console. (This is how we have been handling things in the previous sections)

In the `concurrent()` function, both promises are constructed without using `await`. We then `await` each of their resolutions to print them to the consoles. In other words, we will not print anything with `console.log` until both of the functions have settled.

With the `concurrent()` function, both promises' asynchronous operations can be run simultaneously. If possible, we want to get started on each asynchronous operation as soon as possible.

Within our `async` functions, we should still take advantage of *concurrency*, the ability to perform asynchronous actions at the same time.

*Note: if we have multiple truly independent promises that we would like to execute fully in parallel, we must use individual `.then()` functions and avoid halting our execution with `await`.*
____________________________________________________________________

## Await Promise.all()

Another way to take advantage of concurrency when we have multiple promises which can be executed simultaenously is to `await` a `Promise.all()`.

Remember that we pass an array of promises as the argument to `Promise.all()` and it then returns a single promise.

This single promise will resolve when all of the promises in the argument array have been resolved.

This promise's resolve value will be an array containing the resolved values of each promise from the argument array.

```
async function asyncPromAll() {
  const resultArray = await Promise.all([asyncTask1(), asyncTask2(), asyncTask3(), asyncTask4()]);
  for (let i = 0; i<resultArray.length; i++){
    console.log(resultArray[i]); 
  }
}
```

In our above example, we `await` the resolution of a `Promise.all()`. This `Promise.all()` was invoked with an argument array containing four promises. Next, we loop through our `resultArray` and log each item to the console.

The first element in `resultArray` is the resolved value of the `asyncTask1()` promise, and so on.

`Promise.all()` allows us to take advantage of asynchronicity - each of the four asynchronous tasks can process concurrently.

`Promise.all()` also has the benefit of *failing fast*, meaning it won't wait for the rest of the asynchronous actions to complete once any one has rejected. As soon as any of the promises in the array rejects, the single promise returned from `Promise.all()` will reject with that reason.

As it was when working with native promises, `Promise.all()` is a good choice if multiple asynchronous tasks are all required, but none of them must wait for any other before executing.
____________________________________________________________________

## Summary

- `async...await` is syntactic sugar built on native JavaScript promises and generators.
- We declare an async function with the keyword `async`.
- Inside an `async` function we use the `await` operator to pause execution of our function until an asynchronous action completes and the awaited promise is no longer pending .
- `await` returns the resolved value of the awaited promise.
- We can write multiple `await` statements to produce code that reads like synchronous code.
- We use `try...catch` statements within our `async` functions for error handling.
- We should still take advantage of concurrency by writing `async` functions that allow asynchronous actions to happen in concurrently whenever possible.
____________________________________________________________________

# HTTP Requests

A web page is generated by a mixture of HTML, CSS, and JavaScript, sent to you by the domain via the internet. The internet is made up of a bunch of resources hosted on different servers. In this case, "resource" means any entity of the web including HTML files, CSS stylesheets, images, videos, and scripts, etc. To access the content on the internet, your browswer must ask these servers for the resources it wants and then display these resources to you. This protocol of requests and responses enable you to view a web page in your browser.

This next section will focus on one fundamental part of how the internet functions: HTTP.
____________________________________________________________________

## What is HTTP?

HTTP stands for Hypertext Transfer Protocol; It is used to structure requests and responses over the internet. HTTP requires data to be transferred from one point to another over the network.

The transfer of resources happens using TCP - Transmission Control Protocol. In viewing a webpage, TCP manages the channels between your browswer and the server. TCP is used to manage many types of internet connections in which one computer or device wants to send something to another. HTTP is the command language that the devices on both sides of the connection must follow in order to communicate.
____________________________________________________________________

### HTTP & TCP: How it Works

When you type an address, such as [www.codecademy.com](www.codecademy.com) into your browswer, you are commanding it to open a TCP channel to the server that responds to that URL or [Uniform Resource Locator](https://en.wikipedia.org/wiki/Uniform_Resource_Locator). A URL is like your home address or phone number - it describes how to reach you.

In this situation, your computer, which is making the request, is called the **client**. The URL you are requesting is the address that belongs to the **server**.

Once the TCP connection is established, the client sends a HTTP *GET* request to the server to retrieve the webpage it should display. After the server has sent the response, it closes the TCP connection.

If you open the website in your browswer again, or if your browswer automatically requests something from the server, a new connection is opened which follows the same process described above.

GET requests are one kind of HTTP method a client can call. You can learn more about other common methods, like POST, PUT, and DELETE, in [this article](https://www.codecademy.com/articles/what-is-rest).

Let's dive deeper into how GET requests are used to help your computer access resources on the web.

Suppose you want to check out the latest courses offered on [http://codecademy.com](www.codecademy.com). After you type the URL into your browser, your browser will extract the `http` part and recognize that it is the name of the network protocol to use.

Then, it takes the domain name from the URL, in this case "codecademy.com", and asks the internet Domain Name Server to return an Internet Protocol (IP) address.

Now the client knows the destination's IP address. It then opens a connection to the server at that address, using the `http` protocol as specified. It will initiate a GET request to the server which contains the IP address of the hose and optionally a data payload. The GET request contains the following text:

```
GET / HTTP/1.1
Host: www.codecademy.com
```
This identifies the type of request, the path on [www.codecademy.com](www.codecademy.com) (in this case, "/") and the protocol "HTTP/1.1".

HTTP/1.1 is a revision of the first HTTP, which is now called HTTP/1.0.

In HTTP/1.0, every resource request requires a separate connection to the server.

HTTP/1.1 uses one connection more than once, so that additional content (like images or stylesheets) is retrieved even after the page has been retrieved.

As a result, requests using HTTP/1.1 have less delay than those using HTTP/1.0

The second line of the request contains the address of the server, which is `"ww.codecademy.com"`. There may be additional lines as well depending on what data your browser chooses to send.

If the server is able to locate the path requested, the server might respond with the header:

```
HTTP/1.1 200 OK
Content-Type: text/html
```
This header is followed by the content requested, which in this case is the information needed to render [www.codecademy.com](www.codecademy.com).

The first line of the header, `HTTP/1.1 200 OK` is the confirmation that the server understands the protocol that the client wants to communciate with (`HTTP/1.1`), and an [HTTP status code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) signifiying that the resource was found on the server.

The second line, `Content-Type: text/html`, shows the type of content that it will be sending to the client.

If the server is not able to locate the path requested by the client, it will respond with the header:

```HTTP/1.1 404 NOT FOUND```

In this case, the server identifies that it understands the HTTP protocol but the `404 NOT FOUND` status code signifies that the specific piece of content requested was not found. THis might happen if the content was moved or if you typed in the URL path incorrectly or if the page was removed. You can read more about the 404 status code, commonly called a 404 error, [here](https://www.codecademy.com/articles/http-errors-404).

### Understanding HTTP & TCP with an Analogy

It can be tricky to understand how HTTP functions because it’s difficult to examine what your browser is actually doing. (And perhaps also because we explained it using acronyms that may be new to you.) Let’s review what we learned by using an analogy that could be more familiar to you.

Imagine the internet is a town. You are a client and your address determines where you can be reached. Businesses in town, such as Codecademy.com, serve requests that are sent to them. The other houses are filled with other clients like you that are making requests and expecting responses from these businesses in town. This town also has a crazy fast mail service, an army of mail delivery staff that can travel on trains that move at the speed of light.

Suppose you want to read the morning newspaper. In order to retrieve it, you write down what you need in a language called HTTP and ask your local mail delivery staff agent to retrieve it from a specific business. The mail delivery person agrees and builds a railroad track (connection) between your house and the business nearly instantly, and rides the train car labeled “TCP” to the address of the business you provided.

Upon arriving at the business, she asks the first of several free employees ready to fulfill the request. The employee searches for the page of the newspaper that you requested but cannot find it and communicates that back to the mail delivery person.

The mail delivery person returns on the light speed train, ripping up the tracks on the way back, and tells you that there was a problem “404 Not Found.” After you check the spelling of what you had written, you realize that you misspelled the newspaper title. You correct it and provide the corrected title to the mail delivery person.

This time the mail delivery person is able to retrieve it from the business. You can now read your newspaper in peace until you decide you want to read the next page, at which point, you would make another request and give it to the mail delivery person.
____________________________________________________________________

### So, What is HTTPS?

Since your HTTP request can be read by anyone at certain network junctures, it might not be a good idea to deliver information such as your credit card or password using this protocol.

Fortunately, many servers support HTTPS, short for Hypertext Transfer Protocol Secure, which allows you to encrypt data that you send and receive. You can learn more about HTTPS [here](https://en.wikipedia.org/wiki/HTTPS#Difference_from_HTTP).

HTTPS is important to use when passing sensitive or personal infomration to and from websites. However, it is up to the businesses maintaining the servers to set it up. In order to support HTTPS, the business must apply for a certificate from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority).
____________________________________________________________________

## GET Requests with Fetch API

The first type of requests we're going to tackle is GET requests using `fetch()`.

The `fetch()` function:
- Creates a request object that contains relevant information that an API needs
- Sends that request object to the API endpoint provided
- Returns a promise that ultimately resolves to a response object, which contains the status of the promise with information the API sent back.

Let's walk through the boilerplate code when we use `fetch()` to create a GET request, step by step.

```
fetch('https://api-to-call.com/endpoint').then(response => { 
    if (response.ok) {
        return response.json();
    }
    throw new Error ('Request failed!');
}, networkError => console.log(networkError.message)
).then(jsonResponse => {
    // Code to execute with jsonResponse
]);
```

First, call the `fetch()` function and pass it a URL as a string for the first argument, determining the endpoint of the request.

The `.then()` method is chained at the end of the `fetch()` function and in its first argument, the response of the GET request is passed to the callback arrow function.

The `.then()` method will fire only after the promise status of `fetch()` has been resolved.

Inside the callback function, the `ok` property of the `response` object returns a Boolean value. If there are no errors, `response.ok` will be true and the code will return `response.json()`.

If `response.ok` is a falsy value, our code will throw an error.

A second argument passed to `.then()` will be another arrow function that will be triggered when the promise is rejected. 

It takes a single parameter, `networkError`. This object logs the `networkError` if we could not reach the endpoint at all (e.g. the server is down).

A second `.then()` method will run after the previous `.then()` has finished running without error. It takes `jsonResponse`, which contains the returned `response.json()` object from the first `.then()` method as its parameter and can now be handled however we may choose.
____________________________________________________________________

## POST Requests using Fetch

Take a look at the boilerplate code for a POST request using `fetch()`

```
fetch('http://api-to-call.com/endpoint', {
    method: 'POST',
    body: JSON.stringify({id: '200'})
}).then(response => {
        if (response.ok) {
            return response.json();
        }
        throw new Error('Request failed!');
}, networkError => console.log(networkError.message)
).then(jsonResponse => {
        // Code to execute with jsonResponse
});
```
Notice that the `fetch()` call takes two arguments: an endpoint and an object that contains information needed for the POST request.

The object passed to the `fetch()` function as its second argument contaisn two properties: `method`, with a value of `'POST'`, and `body`, with a value of `JSON.stringify({id: '200'});`.

The second argument determines that this request is a POST request and what information will be sent to the API.

A successful POST request will return a response body, which will vary depending on how the API is set up.

The rest of the request is identical to the GET request. A `.then()` method is chained to the `fetch()` function to check and return the `response` as well as throw an exception when a network error is encountered.

A second `.then()` method is added on so that we can use the response however we may choose.
____________________________________________________________________

## Async GET Requests

Lets take a look at the boilerplate code to set up async GET requests. With this, we take what we learned about chaining Promises and make it simpler using `async...await` syntax, along with `try` and `catch` statements.

```
const getData = sync () => {
    try {
        const response = await fetch('https://api-to-call.com/endpoint');
        if (response.ok) {
            const jsonResponse = await response.json();
            // Code to execute with jsonResponse
        }
        throw new Error ('Request failed!');
    } catch (error) {
        console.log(error);
    }
}
```
- The `async` keyword is used to declare an `async` function that returns a promise
- The `await` keyword can only be used within an `async` function. `await` suspends the program while waiting for a promise to resolve.
- In a `try...catch` statement, the code in the `try` block will be run and in the event of an exception, the code in the `catch` statement will run.
____________________________________________________________________

## Async POST Requests

As we've seen before, a POST request requires more information than a GET request. Let's take a look at the example below:

```
const getData = async () => {
    try {
        const response = await fetch('https://api-to-call.com/endpoint', {
            method: 'POST',
            body: JSON.stringify({id: 200})
        })
        if (response.ok) {
            const jsonResponse = await response.json();
            // Code to execute with jsonResponse
        }
        throw new Error('Request failed!');
    }   catch(error) {
        console.log(error);
    }
}
```

We still have the same structure of using `try` and `catch` as the `async` GET request we just learned about - **but** - in the `fetch()` call, we now have to include an additional argument that contains more information like `method` and `body`.

The `method` property value is set to `'POST'` to specify the type of request we are making. Then we have to include a `body` property wit hthe value of `JSON.stringify({id: 200}).
____________________________________________________________________

## Summary

- GET and POST requests can be created in a variety of ways.
- We can use `fetch()` and `async`/`await` to asynchronous request data from APIs.
- Promises are a type of JavaScript object that represents data that will eventually be returned from a request.
- The `fetch()` function can be used to create requests and will return promises.
- We can chain `.then()` methods to handle promises returned by the `fetch()` function.
- The `async` keyword is used to create asynchronous functions that will return promises.
- The `await` keyword can only be used with functions declared with the `async` keyword.
- The `await` keyword suspends the program while waiting for a promise to resolve.
____________________________________________________________________

# Browser Compatibility and Transpilation

Since everyone uses different browsers and those browsers can be different versions, sometimes a webpage might run fine on one browser but look completely different or just straight up broken on another. 

This is because when browsers interpret and run the code that you make your websites with, if they are not updated they might not recognize some syntax as valid JavaScript code. This causes issues with viewing the website and sometimes will throw an error. 

How do we deal with this? In the following sections, we will cover *browser compatibility* and *transpiliation* as a way to tackle these issues.
____________________________________________________________________

## Browser Compatibility and Modern JavaScript Syntax

When we design a website for browser compatibility, we design it to work correctly for as many different browsers and browser versions as possible.

We can use tools like [caniuse.com](caniuse.com) to provide helpful browser compatibility information for us. We can see things like

- If a browser version supports a certain feature
- What browser versions *don't* support those features
- What percentage of internet users are using these versions

Using this information we can make decisions about how we design our website so that it reaches the largest number of users possible.
____________________________________________________________________

## Introduction to Transpilation

The newer features of JavaScript tend to make it easier to do things rather than add new features, a concenpt known as *syntactic sugar*. We can use older syntax to do the same things but its usually harder to write.

For example, ES6 added string interpolation, allowing variables and expressions to be incorporated into string content:

```
// ES6 string interpolation using template literals
`You can make carbonara with ${pasta}, ${meat}, and a sauce made with ${sauce}.`;

// Pre-ES6 string interpolation
'You can make carbonara with ' +
  pasta +
  ',' +
  meat +
  ', and a sauce made with ' +
  sauce +
  '.';
```
If we wanted to make our JS run on older browsers we would have to make these kinds of changes - but luckily there are tools that can help to automate this process.

If the term *compilation* translates code from one language to another (e.g. when code is compiled from JS to machine), then *transpilation* is the term for translating code to different formats of the same language.

We can use a *transpiler* to covert our modern code into a more compatible version.

Before we publish our code online we can take our source code and transpile it. This produces files that use more browser-compatible syntax.
____________________________________________________________________

## Using Babel

One of the commonly used tools for transpilation is [Babel](https://babeljs.io/). We can use the website version or even integrate it into our projects so that we can run it in a terminal.
____________________________________________________________________

### Babel Configuration

Babel is a Node package, so we need to initialize our npm project using `npm init -y`. This sets us up with a **package.json** file.

Next, we need to install `@babel/cli` and `@babel/preset-env` as devDependences using `npm install --save-dev`.

`@babel/cli` provides the main babel functionality as well as the command line interface. `@babel/preset-env` is a standard way of configuring Babel to transpile all of the common ES6 features, instead of having to listen them one by one.

Babel is configured using a file named `.babelrc`. With `@babel/preset-env`, the content of this file is simple:

```
{
  "presets": ["@babel/preset-env"]
}
```

The **.babelrc** file is saying to use the `@babel/preset-env` configuration. This will transpile the latest adopted JS features into code supported by older browsers.

Next, we want to define the command we will use to run Babel on our project. We will do this by defining a `build` command in the `scripts` section of our **package.json**:

```
"scripts" : {
  "build" : "babel src -d out"
}
```

This is using the `babel` command (from `@babel/cli` with the first argument `src` specifying where the code is we want to run babel on. The `-d` flag is used to specify where we want Babel to store the output, in this case, the **out** folder.

With the command defined, we can run Babel using the `build` command.

```npm run build```
____________________________________________________________________

### Targeting Different Browsers

In addition to providing a fast way to configured Babel, `babel-present-env` allows us to provide a list of browsers we want to be supported using a file named **.browserslistrc**.

Within this file there are many ways we can specify our target list of browsers. A good default configuration, which covers most of the browsers a developer could expect users to be on, can be specified with

```default```

However, we can also customize the list. For example, if we wanted to make sure that our project is supported by the last two versions of Internet Explorer we would write:

```last 2 Explorer versions```

Or maybe we want to make sure the application supports 99.5% of the users on the internet

```cover 99.5%```

The [browserslist documentation](https://github.com/browserslist/browserslist) provides additional syntax and examples for configuring **.browserslist**.

After the file has been defined, we can use the following command to list all the browsers supported:

```npx browserslist```

*Note that although the file is called **browserslistrc** the command to list all the supported browsers is **browserslist** - this is not a typo*
____________________________________________________________________

## Summary

- Changes to JavaScript features over time can result in your modern website not working for users with older browsers, this issue is called *browser compatibility*.
- Modern JavaScript can be *transpiled* into older syntax, making it run on older browser versions.
- A popular Node package for transpiling your project automatically is called *Babel*.
- Babel is configured to target a list of browsers or a percentage of internet users via a **.browserslistrc** file.

Babel can be set up by:

- Initializing your project with `npm init`
- Installing the necessary libraries as developer dependencies:
	- `@babel/cli`
	- `@babel/preset-env`
- Adding a `build` command in **package.json** specifying your source code directory and the output location.
