# JavaScript Notes from Angela Yu Course + Jonas Course

### Problem Solving

- Make sure you 100% understand the problem - ask the right questions.
- Divide and Conquer - Break a big problem, take it apart into smaller problems
- Don't be afraid to do research - stack overflow, MDN docs 
- Write pseudo-code before writing actual code - so that you understand the problem yourself
- To keep clean code, always make sure to define all of your variables at the top of your code.

### Javascript (ES6/ES2015)

- ES is shorthand for ECMAScript (which is the european computer manufacturer's script).
- When creating JavaScript code, make sure that Chrome is always the latest version. Also use Babel to transfile your code to make sure all browsers can use it.
- Java vs. Javascript - no relation whatsoever. Javascript is an interpreted programming language (meaning it kind of translates to the compiled language what to do - starts slowly and you can check how it is going during the process) whereas Java is a compiled programming language (meaning it does the job the interpreter has set out - starts quickly, but you can't really see what is happening throughout).
- Interpreted languages are languages such as Javascript, Python & Ruby - whereas compiled programming languages are like Java, C/C++, and Swift.
- When opening the JavaScript console, to write a double line of code, hold shift and press enter.
- Using the snippet editor of JavaScript console is a great way to write and test your code.
- `alert("Hello");` - the `alert` is the FUNCTION (gets the browser to do something), `"Hello"` is the MESSAGE that you want displayed (AKA the STRING) and the `;` is the END of the instruction so that the browser doesn't get confused between one line and the other.
- - Strict mode: makes it easier for us to write secure javascript mode - `'use strict';` which needs to be at the very top of the code in the script.js file. This will also help to reduce errors in your code.
  - Scopes. Let and const variables are block-scoped, meaning that they can only be accessed inside of the block they are in. var variables can be accessed as part of the global scope, meaning you can grab the var from above and below if needed. The scope chain only works upwards (similar to parents in CSS).
  - Scoping - where does the particular variable live? 


- <strong>PRIMITIVE Data Types</strong>
<ol>
    <li>STRINGS (text we want to be displayed - it is a "string" of characters - these are immutable, meaning they cannot be changed - always put these in double/single quotes)</li>
    <li>NUMBERS (always have decimals i.e. 23.0)</li> 
    <li>BOOLEANS (true/false)</li> 
    <li>UNDEFINED (variable that isn't defined)</li>
    <li>NULL (empty value)</li>
    <li>SYMBOL (value is unique and cannot be changed - not very useful)</li>
    <li>BigInt (for larger integers that the number type can hold)</li>
</ol>

- `typeof` - is an <strong>operator</strong> that tells us what the data type is within the round brackets. I.e. `typeof(true)` would result in a BOOLEAN answer. OR `typeof("Hello")` would result in a STRING answer.
- <strong>Variables</strong> help to make the system "remember" the input.
- `var` is the old way of using JavaScript. You probably want to use `const` and `let` instead. 
- `var myName = "James";` - `var` is a KEY WORD (similar to alert and prompt) to tell us that we are creating a new data container. The `myName` is the NAME OF VARIABLE (which you can also imagine as the box) and the `"James"` is the STRING/VALUE.
- Variable names cannot start with numbers and cannot contain spaces or dashes. It is better to camelCase. They can only contain numbers, letters, underscores or dollar signs - you also can't lead with a number. Never call your variables just 'name'.
- 
- <strong>Values</strong> are either `objects` or `primitive`. 

- <strong>Strings</strong> can be combined using concactenation. `alert("Hello" + " " + "Name");` would mean that it would equate to "Hello Name" on the pop up section.
  
- You can easily find out the number of characters in a string by stating `word.length` `(variablename.length)`
- `var` is pretty much the same as using `let` - BUT there are many differences. 
  
- The <strong>Slice(x,y)</strong> function allows you to slice your strings to seperate them into individual characters. An example:
`var name = "James";`
`name.slice(0,1);` - would mean that the J is being selected. Programmers always start from 0, so although 'James' has 5 letters, S would be 4 (as J is 0). In order to grab the last letter though -
`name.slice(4,5);`
The start of the splice is the first number of the array you want, and the last number of the splice is the end represents where the index stops.
- The `concat()` method can help to combine 2 different types of arrays (and returns a new array). 

- `word.toUppercase()` - can turn every single character in a string to uppercase. Same with `word.toLower`
  
<strong>I am finding this super challenging...</strong>

- <strong>Numbers</strong> - you can add by `+`, subtract by `-`, division by `/`, multiply by `*`, but the <strong>modulo</strong> is represented by a `%` sign. The <strong>modulo</strong> will give you the remainder of the division (see below):
- You can do 'to the power of' by `**` i.e. `2 ** 3`. 
- `var a = 13 % 5; // 3` as this is the remainder of the 2 values when being divided by the number. 5 can go into 13, twice and then whatever is left is the number - i.e. 3. 
- another example: `var a = 16 % 4` would be 0, as there is nothing remaining.
  
- It is good programming practice to add a set of parantheses during BEDMAS protocols with numbers (even when you know this will happen by default).
  
- The <strong>Increment expression</strong> is another way of using `x = x+1` but you would use `x++` (which is the equivalent). `x = x-1` would be the same as `x--` and this would be the <strong>Decriment expression</strong>. You are only ever changing the value by one. If you need to increase by a specific number or variable, then you would use `x +=` and then by the number/variable, same with `x -=`. You can also do this for *, /, etc.
  
- <strong>Functions</strong> allow you to create a set of instructions and package it into a block of code `function getMilk() { }`. Function is the keyword (stating that we are about to create a new function), the getMilk is the function (to identify the new function), the `()` is the parameter/variables that are only specific to the function, and then the instructions will go into the curly brackets (or the function body). 
- Think of functions as machines (like a food processor - put food into the processor which does something to the food, which then returns juice). 
- Function declarations vs function expressions: you can CALL declarations before they are listed in the code, but can't do this with the expression (remember expressions create values). It is good to know how to use both. Function expressions is when the function is assigned to a variable - i.e. `const functionName = function() {}`
  
- <strong>Arrow functions</strong> are another type of function that you can use `=>`. With arrow functions, you drop the "function" keyword and place a `=>` between the `()` and `{}`. If you have a function that is only returning things, you can drop the curly brackets all together.
- If you don't return anything in the curly brackets, the function should automatically return a result. That is the benefit of arrow functions. 
  
- We don't usually console.log the function, we usually use the return. 
  
- There is a difference for when you create the function and USING/CALLING/RUNNING/INVOKING the function. To do this you just would put `getMilk();` into the code. This means the computer will carry out all of the instructions into the curly braces.
- It is important to indent the lines of code inside of the curly braces (or the function's instructions) so that it is easy to tell they are the instructions in the code. <strong>THE CURLY BRACKETS DO NOT NEED TO BE CLOSED WITH A SEMI-COLON.</strong>

- <strong>console.log</strong> will log the string inside the console. The important difference between the alert and console.log is that the alert is something the user can see, whereas the console.log is not. This should be at the bottom.
  
- inputs within functions: `function getMilk(bottles) { }` - this "bottles" is used much like a variable (to contain the input) and you can use this inside of the function to do something with it. I.e. `function getMilk(bottles) { var cost = bottles * 1.5; }`. When calling, `getMilk(2)` then bottles would = 2. Cost of the bottle will then be 3.
  
- <strong>Floor Method</strong> is when you can ensure that a value is always rounded down to fit a "whole number" as opposed to 3.33 bottles of milk for example. You would need to do it like this: `var numberOfBottles = Math.floor (money - 1.5);`. The `Math.floor` if the floor function.
- the Math.floor function rounds a number down to the nearest integer, whereas the Math.random function generates numbers from 0 to 1.
- `Math.floor(Math.random() * 5) + 1;.` - would give a random number between 1 and 5. 

- Math.random will generate are random number (between 0 and 0.9999). 
  
- There are also functions that are able to take an input and are able to use this inside the function to do something (or able to give an output).
- In order to get an OUTPUT out of the function, you need to use the `return` keyword. When we then CALL a function that has an output, we can use the output and assign it to a variable. This is usually added just before the closing brace i.e. `return money % 1.5;` which will give you the remainder of the division.
- The `return` keyword will actually 'exit' the function, meaning the function is done (meaning it has returned).
- This means you can't put anything after the return keyword, as it will be ignored (you'd have to put it above the return).

- <strong>Data Structures</strong> - the most important are Arrays and Objects. 
  
- <strong>Arrays</strong> are MUTABLE components (meaning you can change the value of them using the index indirectly - even if they are CONST) `["first", "second", "third"]` that can hold a series of values (like a container) (it is non-primitive data, meaning they can hold much more complex data - primitive data are numbers and strings which can only hold one value at a time).
- There are different ways to write arrays. Example 1:
-     `const friends = ["Michael", "Steven", "Peter"];` - more common.
-     `const friends = new Array(Michael, Steven, Peter);`
- To find out how many elements are in an Array, you would use console.log(variable.length) - and in the first example, the answer would be 3 as it starts from 1. 
- To access a value in your <strong>Array</strong>, you want to use the index (which means the first value will be `array[0]` which would mean 0 would be `"first"` for example. These start at 0 so first would be 0. 
- To get the last element in an array (as sometimes we do not know how many values are in an array), you can use the <strong>.length</strong> property via `array[array.length - 1] = 10 (or whatever value you want to change to)`.
  
- <strong>Methods</strong> are functions associated with certain values/objects (e.g. `.log()` is a method for the `console` object). Arrays have their own methods. They will require paranthesis. 
- `.push()` method is the first method associated with arrays and it allows you to "PUSH" or add a value to the end of an array. i.e. `arrays.push("value")` will add "value" at the end of your array. `.push()` will return the new length of the array, after adding the value you give it.
- The `unshift` method allows you to add a value to the start of the array. I.e. `arrays.unshift`. The `shift` method allows you to remove a value at the start of the array and return it back to you. 
- `.pop()` method allows you to remove the last element and returns this element back to you. You don't need parameters into this
- `indexOf()` can tell you what number in the string the value is that you want. I.e. `console.log(friends.indexOf("Steven"));`. If an element is not in there, it will be -1 in the console. You likely need to pop this one in the console.log. 
- To find out if an element is in the array or it isn't, you can use the `.includes()` method. I.e. `console.log(friends.includes("Steven"));` this will come out in 'true' if it is in there, 'false' if not.
- Common example of `.includes()` is in if/else statements. I.e. `if (friends.includes("Steven")) {console.log("You have a friend called Steven");` would be true.
- The `shift` method allows you to remove the first element of an array.
- The `concat` method can add two arrays together to create a new array.
- The `forEach` method is used to execute a function for each item in an array.
-     array.forEach(function(item) {
  // code to execute for each item
  });
- With the `forEach` method, you don't define a new function, you just use the function keyword.
- The `reduce()` method can help you to reduce an array to a single value by applying a function to each element in the array.
  
- Using the `let` keyword on a variable, allows for the variable to be re-assigned/mutated. Using a `const` variable, means that it will not be able to be reassigned in the code. You can also not have 'empty' `const` variables.
- <strong>It is best practice to always use `const` as it is the best way to avoid any bugs in the future</strong>.
- `+` `-` `*` `**` `=` `+=` `*=` `/=` etc are all operators.
- <strong>Operators</strong> can be seen through this resource on a table of precedence - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence
- Assignment operators go from RIGHT to LEFT. Math operators go from LEFT to RIGHT.

- <strong>Comparison operators</strong> are used to produce boolean values. This can be the `>` operator asking if one variable is greater than the other (will produce either true or false). Can also be `<` `<=` `>=`. These are usually a little lower than math operators in precedence.

- <strong>Template literals</strong> use back ticks `` to create a string. This is a way to avoid having to add additional spaces, and having to keep re-doing this over time. 
- Instead of: const james =
  "I'm " + firstName + ", a " + (year - birthYear) + " year old " + job;
- It would be: const jamesNew = `I'm ${firstName}, a ${year - birthYear} year old ${job}`;

- <strong>if</strong> statements: check snippets in folder.
- <strong>else</strong> statements: check snippets folder - will usually be executed if the `if` statement is false.
- These are called if/else control structures.

- <strong>Type conversion</strong> - when we want to convert from one type to another. For example: if you have a string 'const inputYear = 1995' it isn't a number so you may have to convert it to a number. To do this `console.log(Number(inputYear)); this should convert it to a number.
- You can also do the above with a String function (just replace the Number). 
- NaN - "not a number".
- <strong>Type coercion</strong> - happens whenever an operater is dealing with a value of two different types. JavaScript will do this in the background. I.e. It usually converts numbers into strings if you concatenate numbers and strings.
- It's important to know that the `+` will only convert a number to a string, and not the other way around like `-`, `/` and `*` would. I.e. if you have `const n = '1' + 1`, JavaScript will make this into a string of 11. Doing `const n = '1' / 1` would = 1.
  
- There are 5 falsy values - 0, undefined, NaN, '', and null.
- `console.log(Boolean(0));` would be 'false' - the opposite will be 'truthy'.
- A 'truthy' value is considered true when evaluated as a boolean. Most values are truthy. 

- <strong>Equality operators</strong> include `===` and `==`. The `===` is a strict equality operator, and does not perform type coercion (whereas `==` does as it a loose equality operator - meaning it can convert string to number).
- As a general rule, always use `===` as it helps to avoid bugs in the future as a default.
- The <strong>different</strong> operator is represented as an `!==`.

- <strong>Boolean logic</strong> - these are the `AND - &&` operators and `OR - ||` operators. For an `AND` operator to be true, all outcomes will need to be true (vice versa). For the `OR` operator to be true, only one variable needs to be true. The `NOT - !` operator will invert the variable (i.e. if it is true, it will become false). The not operator is `!Variable`. The NOT operator has precendence over the AND and OR operators.

- <strong>Conditional/ternary operators</strong> are used to write if/else statements in shorter amount of code. These are expressions.
- `console.log(BACKSLASH I like to drink ${age >= 18 ? "wine" : "water"}BACKSLASH);`
- The `?` indicates the IF STATEMENT PART and the `:` indicates the ELSE STATEMENT PART. Remember the `${}` are template literals.
- The turnary/conditional operators are perfect for taking a quick decision

- Expressions produce values, whereas statements are bigger pieces of code which do not produce a value (such as an operator). Examples of statements are 'if else statements' and 'switch statements'. Statements end in semi-colons.

- 3 weeks off - a little worried to get back into it just in case I forgot everything (:

- <strong>OBJECTS</strong> - can define <strong>key (variable name)</strong> value pairs. Instead of Arrays using the square brackets, you would use the curly brackets to define the object.
- The object name is called the key, whereas the amount of items in the object are called properties.
- These are the most fundamental concepets in the javascript language.
- We use objects to group together different variables that belong together.
- The difference between arrays is that in arrays, the order where we specify elements matters a lot (using order numbers) - usually more ordered data, whereas objects it doesn't matter about the order.
- <strong>Dot vs. Bracket notations</strong> are ways to retrieve properties from an object. i.e. `console.log(james.lastName)` - if you wanted to receive the lastName from an object for example (this would be the dot notation) or `console.log(james['lastName'])` would be the bracket notation. In the square brackets, you can put any notation in there - i.e. strings - this would only work for bracket notations. Dot notations are usually cleaner. 
- We can also add function expressions to objects as a METHOD. To do this, you wouldn't add `const calcAge = function()` you would just do `calcAge: function ()`.
- To call a function with the brackets, you would do the following: `console.log(james["calcAge"](1995));`
- 
  
- `for` <strong>loops</strong> are used when you have to repeat a task multiple times. Loops need an <strong>iterator/counter</strong>, which is a variable you can declare specifically in your loop to control how the loop iterates (or goes through logic). This is usually `i`. 
- `for` loops will keep running while the condition is TRUE. This can create a loop for an infinite amount of times (whereas `while` loops are used when it is needed for an infinite amount of times). 
- `for (let rep = 1; rep <= 10; rep++) {
  console.log(BACKSLASHLifting weights repetition ${rep}BACKSLASH);`
- `let rep = 1;` would be the start, `rep <= 10;` would be the end, and `rep++` would be whether it is going up or down. 
- One of the most common uses of loops is to loop arrays.
- When looping arrays, as they are zero-based, it is important to class it as 0 - `for(let i = 0)`. 
- It is common to use `i` as your iterator variable. `for ("iterator"; "condition"; "iteration") {}`.
- `condition` tells the loop how many times it should iterate. When the condition becomes false, it will stop (BOOLEAN value = true/false).
- `<` is a less than operator which allows you to check if the value on the left is less than the value on the right. Usually an answer of true or false.
- `iteration` is a statement at the end which will tell the loop what to do after each run.
- `continue` is a keyword meaning it can exit the current iteration of the loop (OR SKIP AN INTERATION). 
- `if (typeof james[i] !== "string") continue;` - this means if the type of the element IS NOT a STRING, then continue.
- `break` is a keyword that will completely terminate the whole loop.
- Check important screenshots file for examples of this (+ for loops inside of a loop).
- `while` loops - you only need the CONDITION. This will run WHILE the condition is true. These are more versatile than the `for` loops as they don't need a counter/iteration. Please check screenshots for examples. 
- i.e. `while (something is true) {do something}`.
- A big difference between `for` loops and `while` loops is that in `while` loops you will have to directly specify the `i++`. 

- Inside the body or curly brackets of the loop, should be the console.log(i) usually - take this with a grain of salt though until later in my learning.
- A `for...of` statement executes a loop that operates on a sequences of values from an iterable object (arrays and strings) and temporarily assigns it to a variable. `for (const value of iterable) {}`
- `\n` is an escape sequence/new line. THis is the old way of creating a new line, however you can now create a new line with back ticks, just by starting a new line in the code.

### DOM Manipulation
JavaScript interacts with HTML via DOM (Document Object Model). This is a tree of objects that represents the HTML. To do this you can use the `document` object and to find specific elements you would use the `querySelector()` which takes a CSS selector as an argument, and returns the first element that matches the selector. 
- The DOM is not a part of JavaScript, it's actually a part of Web API's (application programming interface - which are libraries that occur behind the scenes). 

- E.g. (to find the h1 element): `let h1 = document.querySelector("h1");`
- In order to use the query Selector for all elements (i.e. if multiple elements have the same class, then you would use `.querySelectorAll`. 
- The above should be encased in a string i.e. for an ID: "#h1".
- The `getElementId` is a lot faster than using query selector and '#h1' for selecting ID's. 
- The `.textContent` property sets the text content of an element and all of its descendants. The `.innerText` property only sets the text content of visible elements of all of the element's descendants. `.textContent` is usually faster.

- The `.value` property can be useful for getting the value for inputs for example.

- The `.addEventListener()` method will need to pass in the type of the event i.e. `click`. It would then need a function as an argument after the type of the event.
- i.e. `document.querySelector('.check').addEventListener('click', function () {
  console.log(document.querySelector('.guess').value);
});` - we also do not call the function. The Javascript engine will call the function as soon as the event happens.
- The first scenario is to always assume that there will be no input, so this will need to be actioned to ensure that your application runs smoothly. 

- You can use the `.onclick` property to determine what something does on the click of a mouse.
- Example: `button.onclick = myFunction;`
- The `innerText` property controls the text that appears in the HTML. I.e. if the ID was #info -
  `const info = document.querySelector("#info"); 
    info.innerText = "Hello World"; ` - whatever the #info text previously was, the innerText would change it to "Hello World".
  - dot notations and bracket notations are ways you can access properties of an object. A dot notation is when you know the name you are trying to access ahead of time - i.e. To read the `name` property of a `developer` object: `console.log(developer.name)`.
  - The bracket notation is when you are trying to access a property that has spaces in it - i.e. `"Space name"` would be `console.log["Space name"];`
  - To add on top of an already existing string (i.e. in a function) use the += operator.
  - The `style` property is used to change the inline style of an element.
  - You can add or remove classes to an element using JavaScript by using `classList.add` or `classList.remove` and even toggle using `classList.toggle` to toggle on and off the style/action. Whenn adding/removing a class, you don't need to use the "." before the new class. 
  - The `display` property is used to set the visibility of an element.
  - Example: `const monsterStats = document.querySelector("#monsterStats");
              monsterStats.style.display = "block";`
  - The `innerHTML` property allows you to access or modify the content inside an HTML element using JavaScript.
  - When adding in new lines `\n` you would need to concactenate it and put it in brackets usually.
  - Responding to keyboard events - still need to use `addEventListener`. You would need to add a global event which would be `document.addEventListener`. You would either use `keydown`, `keypress`, or `keyup`. You would usually use `keydown`. 

- <strong>Hoisting</strong> - Makes some type of variables accessible in the code before they are actually declared.
- Function declarations will be hoisted meaning that you can use them before they have actually been declared (remember that function declarations are block scoped in 'strict mode').
- Var variables will be hoisted, we will get 'undefined' though. This is a common source of bugs in JavaScript, this is why we barely use var.
- Let and const variables, will not be hoisted (these will be placed in a temporal dead zone/TDZ). So if we use a let or const variable before we declare it, it will come up with an error.
- Function expressions and arrow functions will depend on whether using var, const or let. This is why we can't use function expressions before we declare them in the code.
- The temporal dead zone makes it easier for us to find bugs and to make const variables like we are supposed to (as const should never be re-assigned).

- <strong>This</strong> keyword is an extremely important concept to get. It is a special variable made for every execution context and therefore every function. It will always take the value of the owner of the function (points to the owner function).
- It is basically asking 'who is invoking me?' - it will always point to the object calling the method. 
- The value of the <strong>this</strong> keyword is not static (very dynamic), and is only defined when it is called.
- The 'this' keyword can refer to the object in the code via a <strong>Method</strong>. 
- <strong>Arrow functions do not get their own 'this' keyword.</strong>
- If you're ever unsure of the 'this' is inside of a function, you can console.log it to check.
- The 'this' keyword in the global scope will likely be the window object.
- <strong>Never use an arrow function as a method</strong> as it can help to avoid bugs - always use a function expression/declaration (same with not using 'var'). 
- A regular function call has the 'this' keyword set as 'undefined'.
- An arrow function inherits the 'this' keyword from the parent scope, and this can be used as a solution sometimes.
- Think of 'this' like a name-tag. When you call a function with object.method(), you're handing the function a name tag saying, "Hi, I'm object.". But if you say just method() — there’s no name tag. So JavaScript either puts on a generic one (window) or nothing at all (undefined in strict mode).

- <strong>Array destructuring</strong> - to receive variables from an array by declaring a new variable.
  
- Basic destructuring:

`const arr = [1, 2, 3];
const [a, b, c] = arr;`

`console.log(a); // 1
console.log(b); // 2
console.log(c); // 3`

 - To skip elements you would add `[first, , third]` for example.
 - To get elements from nested arrays:

`const ratings = [['rating', 4.19], ['ratingsCount', 144584]];
const [[, rating], [, ratingsCount]] = ratings;`

- <strong>Object destructuring</strong> - we always use the curly braces and provide the variable names that contain the exact property names. I.e.
  `const { name, categories, openingHours } = restaurant`
- You can also include arrays into this `[]` and if you want to rename an object you can do the following:
  `const {name: restaurantName} = restaurant`.
- In order to reassign/mutate variables in an object i.e. const obj = { a: 32, b: 7); - you would need to do `({a, b} = obj})` - so wrapping it in paranthesis. 
