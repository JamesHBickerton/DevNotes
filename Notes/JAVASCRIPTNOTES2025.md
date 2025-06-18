# JavaScript Notes from Angela Yu Course + Jonas Course

### Best Way to Plan a Project 

1. <strong>User Stories</strong> - will clearly describe the functionality of the application from the user's perspective. A common format could be `As a [type of user], I want [an action] so that [a benefit]`. I.e. "As a user, I want to log my workouts with location, distance, time, pace and steps/minute, so I can keep a log of all of my running". 
2. <strong>Features</strong> - User stories will allow us to think of the features. I.e. "Map where user clicks to add new workout", "Search results with input field", "bookmarking functionality", "user can upload files/recipes" etc. 
3. <strong>Flow chart</strong> - what we're going to build - should contain the features, how the different parts of the app react with each other and how the data will flow across the application. It's always a good idea to start with events - i.e. the page loading - "get current location coordinates --> render map on current location". This is only what the program should do, not how it does it.
4. <strong>Architecture</strong> - how we are going to build it. Can have a look at section 15: 248 - project architecture is a good idea. 
5. <strong>Development</strong> - implementing the code. 

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
    <li>BOOLEANS (true/false) - just a note: can be common practice to list variables as `isRandom` or `hasCompleted`</li> 
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

- `word.toUppercase()` - can turn every single character in a string to uppercase. Same with `word.toLower` - HAVE A LOOK AT USEFUL SCREENSHOTS FOLDER.
  
<strong>I am finding this super challenging...</strong>
  
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
- `indexOf()` can tell you what number in the string the value is that you want. I.e. `console.log(friends.indexOf("Steven"));`. If an element is not in there, it will be -1 in the console. This only checks for one character at a time. 
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
- These are called if/else control structures/statements - if/else statements aren't actually used as much anymore. Usually just (in modern JS) would be multiple if statements. 

- <strong>Type conversion</strong> - when we want to convert from one type to another. For example: if you have a string 'const inputYear = 1995' it isn't a number so you may have to convert it to a number. To do this `console.log(Number(inputYear)); this should convert it to a number.
- <strong>UPDATE:</strong> you can actually use the + instead of Number() now as it is a strategy to tell Javascript to do type conversion. 
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
- The turnary/conditional operators are perfect for taking a quick decision. It is actually better to use ternary or logical operators instead of if statements. Instead of doing if/else statements, it is also even better to use more if statements (without the else/if). 

- Expressions produce values, whereas statements are bigger pieces of code which do not produce a value (such as an operator). Examples of statements are 'if else statements' and 'switch statements'. Statements end in semi-colons. GO BACK TO THEORY LECTURE AROUND SWITCH STATEMENTS, NOT SURE WHY I HAVE NO NOTES FOR THIS. 

- 3 weeks off - a little worried to get back into it just in case I forgot everything (:

- <strong>OBJECTS</strong> - can define <strong>key (variable name)</strong> value pairs. Instead of Arrays using the square brackets, you would use the curly brackets to define the object.
- It is good practice not to use arrow functions in objects (as they won't get access to the 'this' keyword in the object). 
- The object name is called the key, whereas the amount of items in the object are called properties.
- These are the most fundamental concepets in the javascript language.
- We use objects to group together different variables that belong together.
- The difference between arrays is that in arrays, the order where we specify elements matters a lot (using order numbers) - usually more ordered data, whereas objects it doesn't matter about the order.
- <strong>Dot vs. Bracket notations</strong> are ways to retrieve properties from an object. i.e. `console.log(james.lastName)` - if you wanted to receive the lastName from an object for example (this would be the dot notation) or `console.log(james['lastName'])` would be the bracket notation. In the square brackets, you can put any notation in there - i.e. strings - this would only work for bracket notations. Dot notations are usually cleaner. 
- We can also add function expressions to objects as a METHOD. To do this, you wouldn't add `const calcAge = function()` you would just do `calcAge: function ()`.
- To call a function with the brackets, you would do the following: `console.log(james["calcAge"](1995));`
  
  
- `for` <strong>loops</strong> are used when you have to repeat a task multiple times. Loops need an <strong>iterator/counter</strong>, which is a variable you can declare specifically in your loop to control how the loop iterates (or goes through logic). This is usually `i`.
- It is actually good practice to avoid using loops (just important to know how to do them). It is better to use array methods instead (like map, filter and reduce). 
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

- `\n` is an escape sequence/new line. THis is the old way of creating a new line, however you can now create a new line with back ticks, just by starting a new line in the code.

### DOM Manipulation
JavaScript interacts with HTML via DOM (Document Object Model). This is a tree of objects (kind of like the interface) that represents the HTML (and allows us to make JS to interact with the browser). To do this you can use the `document` object and to find specific elements you would use the `querySelector()` which takes a CSS selector as an argument, and returns the first element that matches the selector. 
- The DOM is not a part of JavaScript, it's actually a part of Web API's (application programming interface - which are libraries that occur behind the scenes).

- How the DOM API is organised - every single Node is of the type, Node. Each Node is represented by an object.
- There are different types of Nodes - Elements, text, comment and document.
- The document node type is another type of node that contains important methods like querySelector (this is available both on document and element types of nodes). 

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
  - In an event handler function, the 'this' keyword always points to the element it is attached to. I.e. the 'this' keyword will point to a button etc.


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

- <strong>The spread operator '...' </strong> allows an iterable (arrays, strings, maps, sets) to be expanded into individual elements or properties. It's commonly used to copy, combine or pass values without mutating the data. 
- This is similar to destructuring, however the spread operator spreads elements into individual parts (can copy/merge data, and pass multiple values into functions). Destructuring pulls out values from arrays, or properties from objects and assigns them to new variables. You also cannot destructure a function, whereas you can use the spread operator on functions.
- Just a note - the spread operator can work on OBJECTS TOO (which isn't a iterable).

- The <strong> rest operator </strong> goes on the LEFT side of the `=` operator. The rest operator is used to gather multiple elements into a single array or object (collecting function arguments or destructuring). It basically collects the unused (or the rest) elements in the destructuring assignment. It does not include any "skipped" elements i.e. `[first, , third]` - it wouldn't include the `, `. It must always be the last in the destructuring assignment. I.e. `const [pizza, , risotto, ...otherFood] = []`.
- The <strong> rest argument </strong> is used within a function to compress elements. I.e. `const add = function(...numbers) {}` - so it is put through as an argument.

- The difference between rest operators and spread operators is that the spread operator is used where we would use values seperated by comma's, the rest operator is used where we would use variables seperated by comma's.

- <strong> Short circuiting </strong>
- The OR operation (||) - if the first value/operant is a 'truthy', the other variable won't even be evaluated. If there are many parameters, it will return the FIRST truthy value.
- The AND operator (&&) will do the exact opposite and will return the first value/operant is a 'falsy' value.
- The nullish coalescing operator `??` - works with the concept of nullish values instead of falsy values (null and undefined - not 0 or ' '). Only nullish values would short circuit the values.
- The `??` operator checks whether the value on the left side is null or undefined. If it is not, then the left hand value is returned. If it is, then the value of the right is returned. 
- Just to note - `&&` has a higher precendence than `||`

- <strong>Logical assignment operators</strong>
- The `||=` LOGICAL OR - assigns a value to a variable only if the variable is a 'falsy' value. I.e. `a ||= b;` - "this would mean, if a is falsy, then assign b to a".
- We also have the `??=` LOGICAL NULLISH ASSIGNMENT OPERATOR - this will assign a value to the variable if the variable is 'nullish' - i.e. null or undefined.
- We also have the `&&=` LOGICAL AND OPERATOR - this will assign a value to a variable if the variable is truthy.

- <strong>For...of</strong> loops can loop over entire arrays, and can give us access to the current array element that you can specify before the 'or' statement. You don't need to create a code block unless you have multiple lines.
  
  `for (const element of iterable) {
  // Code to run for each element
  }`

- the element represents the current value in the loop, while the iterable is the data structure you are looping over (i.e. string or array).
  
- The `entries()` method returns an iterator that gives you `[index, value]` pairs for each element in the array.

`const fruits = ["apple", "banana", "cherry"];
for (const [index, value] of fruits.entries()) {
  console.log(index, value);
}`

- Optional chaining - if a way of using `?.` to check if a variable or method exists. For example, if you use:
-  `const city = user.profile?.location?.city;` - this would check if first user.profile exists, and then if the location exists - then it will return the city value. If anything is missing it just returns undefined instead of throwing an error.
-  These can also be used for methods - i.e.
-  These are frequently used with the `??` to ensure that there is another option/operant. - IMPORTANT
-  These can also be used on arrays - i.e. `const users = [{name: 'James', email: 'hello@james.com'}]
    console.log(users[0]?.name ?? 'User array empty'):` - this will assess whether the value on the left `users[0]` exists, this would help to avoid having to use if/else statements all the time.

- In objects, We can loop over property names (keys) and property values. You can use this with the `Object.keys` for properties, and `Object.values` for values.
- To loop over both the property names (keys) and values in objects, you would need the entries().
- Remember, you can't use .entries() directly on an object. You would have to do Object.entries(fruits) if an object. 

- <strong>Sets</strong> - to create a new set you type in `= new Set([])` after declaring a variable. A set is a set of unique elements without duplicates.
- The main use of sets is to remove duplicate values of arrays. 
- The length of sets are found using `Set.size` and the includes is `.has` method.
- The .push of sets are `.add` and to remove elements are `.delete` and to delete all of the elements from the set `.clear`.
- Because sets are iterables, we can loop over them. 
- There are no ways of getting data out of a set, and they do not have an index.
- CHECK USEFUL SCREENSHOTS ON HOW TO REMOVE DUPLICATES. 
- The spread operator can also use on sets to unpack sets into a new array.
- The `.intersection()` method can find out what two elements that are common in different groups/arrays - this is extremely useful when converting sets to arrays.
- The `.union()` method will combine all of the elements (apart from duplicates) into one set. This is different from the ...spread operator as it will get rid of all of the duplicates.
- The `.difference()` method will give us all of the elements that are unique in the first set (so order matters). 
- The `.symmetricDifference` which is the opposite of the .intersection method - will give us all of the unique elements.
- There are also other methods that you can use - i.e. `.isDisjointFrom`.

- <strong>Maps</strong> - data structures we can use to map values to keys (just like in objects). The difference between objects and maps, is that the maps can have any types of keys.
- `const variableName = new Map();` - to fill out the map, we can then use the set method. `variableName.set('name', 'James)` - doesn't have to be a string.
- It also returns the map - by getting `variableName.get()`.
- To check if a map has a certain key you would use `variableName.has()` and to delete `variableName.delete()`.
- Maps also have the size property `variableName.size`.
- To convert objects to maps, you can use the Object.entries().
- Iteration is also common on Maps as they are iterables, and can use the loops.
- To convert maps into arrays, you would want to use the spread operator `console.log([...variableName]);`

- <strong> Choosing Data Structures </strong>
- If you need a simple list of values use an array or set (when we don't need to describe the values).
- Always use arrays whenever you need to store values in order and when they may contain duplicates. Sets should only be used if high performance is really important or when there are no duplicates (sets can be 10 x faster than arrays). Sets are usually needed to compliment arrays.
- If you need key value pairs, you would use an object or map. 
- Maps are better suited for key value stores as they allow for better performance (they can also have many data types and easy to iterate, when you need keys that are not strings). The biggest advantage of objects is due to them being more simple to write and if you need methods and using the 'this' keyword.

- <strong>Strings METHODS ADVANCED </strong> are also zero based. In the string, if there are spaces, the spaces will count for the position - if using indexOf for example.
- The <strong>Slice</strong> method - needs indexes as arguments. The slice works a little differently. For example: `const airline = 'Air New Zealand` if using `airline.slice(4)` it would result in the console as `New Zealand` as it would start at 0 (A) and finish at 4 (N), only logging a 'substring'. This will not change the underlying string as it is IMPOSSIBLE to mutate strings, you would need to store it into a seperate value, as they are primitive values.
- The `airline.slice(4)` would have the first value as the `begin parameter` - you can also provide an end parameter i.e. `airline.slice(4, 7)`. It stops extrating before reaching index number 7. The length of the extracted substring will always be `7 - 4 = 3 (in this example)`. 
- To use the slice on an object that you potentially don't know the index of, use the indexOf and lastIndexOf to find this (CHECK USEFUL SCREENSHOTS FOLDER). 
- You can also use minus numbers to get numbers from the beginning parameter and/or ending parameters.
- Whenever we call a method on a string (which technically isn't possible), javascript will turn this string into an object (called boxing - as it takes our string which creates an object. When it is completed, it returns it back to a string).
- You can use `.trim()` - to remove white space from both ends of a word (you can also use the variant `.trimStart()` and `.trimEnd()`.
- The `.replace` can be used on strings to remove one key and replace with the other.
- I.e. `const priceUS = priceGB.replace('£', '$')` - would mean that the £ would be replaced by the dollar sign.
- These can be entire words or single characters, and can be chained. It will only replicate the very first occurence of the word. There is a `.replaceAll()` method that will replicate all of the occurences of the word. 
- Some useful methods for strings are the `.includes()`, `.startsWith()`, and `.endsWith()` - which will return boolean values. These are especially helpful in conditionals (if/else etc).
- It is important to translate all words into lower case when getting inputs to make it easier to match up with your code.
- Also have a look at `.join()`, `.split()`, `.padStart()`, `.padEnd()`, and `.repeat()`.
- The `.padStart()` can be quite beneficial for strings -
`const str1 = "5";
console.log(str1.padStart(2, "0"));
// Expected output: "05"`
- You can do this on numbers too, but obviously would have to use the String() to convert it. 

<strong>Advanced Functions</strong>
- Javascript does not have 'passing by reference', only 'passing by value' - unlike C++.
- A higher order function is a function that receives another function as an argument, that returns a new function, or both.
- There are no first class functions in practice, it's just a concept - there are higher order functions because the langauge supports first class functions..
- For higher order functions, one of the parameters would have the `fn` parameter.
- A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
- JS uses call back functions all the time - this is because it makes it easy to split up our code into more reusable code.
- Abstraction is an important notion to consider - it involves simplifying complex systems by hiding unnecessary implementation details and exposing only essential information to the user.
- `.bind()` method can explicitly define the 'this' keyword for any function call. <strong>It returns a new function</strong> where the 'this' keyword is bound. I believe that this would be assigned to a variable (different to .call and .apply). I.e. `const bookJS = book.bind(jetstar);`. In the bind method you can also pass many arguments. THIS IS EXTREMELY IMPORTANT. 
- `.call()` method the first argument is what we want the 'this' keyword to point to, and then the rest of the arguments. This allows us to explicitly define the this keyword in any function that we want.
- The `.apply()` method does pretty much the same thing as the .call method, but it doesn't have any arguments after. It takes an array of arguments instead to pass it into the function. <strong>It's not really used as much anymore!!</strong> - this is because you can just use the `spread` on the `.call()` method.
- In partial application, many times we are not that interested in the 'this' keyword. This means that we can preset parameters. I.e. using null for objects.
- <strong>Immediately invoked function expressions</strong> are functions that you only want to run once, and then they disappear. To do this (check important screenshots). These aren't really used much anymore.

- <strong>Execution contexts</strong> - The global execution context is created for top level code. An execution context is the environment in which a piece of javascript is executed (like a pizza inside of the box - the box is the execution context and the pizza is the javascsript is the pizza). There is one execution context for each function, and for each function call a new execution context is created. All of these execution contexts will make up the call stack!! Inside of each execution context will contain of a variable environment. Each execution context will also store the scope chain and the 'this' keyword (obviously apart from the arrow functions - that being the this keyword and arguments). 
- </strong>Call stack</strong> - are stacks of execution contexts on top of each other to let us know where we are in the execution (the one on top of the stack, is the one that is currently running). When it is finished running, it will be removed from the stack and go back to the previous execution context.
- <strong>Scopes</strong> - 3 types of scopes. Each variable will always have access to all of the variables from all parent scopes. "sibling scopes" can not have access to each other's variables, only of parent scopes - this is due to lexical scoping. 
  <ol>
    <li>Global scope - if the code is outside any function or block (and are available everywhere in the code).</li>
    <li>Function/local scope - variables are only accessible inside of the function - these are quite weird.</li>
    <li>Block scope - (anything in curly braces i.e. loops etc - these only apply to variables with LET or CONST). If you declare a variable via VAR, then this will still be accessible outside of the block - to the current function or global scope. Var is function/local scoped. Functions are always block scoped (when using strict mode). </li>
  </ol>

- <strong>CLOSURES</strong> - closures happen automatically, we just need to recognise these situations.
- Closures allow asynchronous functions (like event listeners, timers, promises) to “remember” the context they were created in.
- A closure gives a function access to all of the variables of it's parent function, even after that parent function has been returned. This preserves the scope chain throughout time.
- <strong> CLOSURE ANALOGY </strong> - A closure is like a back pack, that a function carries around whereever it goes. This backpack contains all of the variables that were present in the environment where the function was created (think of it as like the function is leaving home - the home is where the function was created, and it is taking all of the variables that were present at its birth place).
- The closure sees the latest value of the variable, not the value at the time of creation. 

- Here's a quick mental checklist when you're debugging closures:
✅ Where is the function defined?
→ That determines what it closes over.

✅ What variables are in scope at that time?
→ That's what gets "remembered."

✅ Is the variable redefined later somewhere else?
→ If it's not in the same scope, it doesn't affect the closure.

### Advanced ARRAYS

- We can use the slice method similar to the strings. Using slice on arrays does not mutate the array but creates a new array (shallow copy of the array with the extracted parts).
- Obviously using the minus in the slice method `arr.slice(-1)` would return the last letter/input.
- You can use the `splice` method which is similar to the slice method, but it actually mutates the array, rather than creating a new array. This would delete the elements that you return into splice, and the original array loses their values. The second value is different from the slice method, in that the last number is 'deleteCount' meaning that it is the number of elements you want to delete. 
  
- The `reverse()` method can be used to reverse the elements of an array, and same as splice it will mutate the original array.
- The `concat()` method can be used to concatinate two arrays. i.e. if you have `arr1` and `arr2` and you wanted to joint arr1+arr2, then you would write `arr1.concat(arr2)` and define that to a new variable. The concat doesn't mutate arrays.
- The `join()` method will work the same as for strings.
- The `at()` method can be used instead of the brackets notation to access one element from an array. If you want to get the last element of the array, you should probably use the at() method. The at method also works on strings. 
- <strong>Ways to get the last element of an array:</strong>
-   `arr[arr.length - 1]` OR `arr.slice(-1)[0]` OR `arr.at(-1)` - the `at()` one being quite easy.
- Just a note: a good way to remove the '-' from values is the `Math.abs`.

- The `forEach()` method is a higher order function that has a callback function. It is the forEach method that will call the callback function. The forEach method will loop over the array, and in each iteration it will execute the callback function. It will pass in the current element of the array as an argument.
- For examples in the parameters for the `forEach()` function, the first one always has to be the `current element`, the second `current index`, and the third `the entire array you are looping over` - obviously can have any name you want in the parameters though.
- The difference between forEach and for of loops is that you cannot break or continue using the forEach loop.
- <strong>I am finding forEach loops much easier to understand than all other types of loops tbh. Will definitely be using these more going forward!!</strong>
- You can also use forEach loops on maps and sets. The first parameter is the current `value`, the second value is the `key`, and the third is the entire `map` that is being looped over.
- REMEMBER sets do not have keys or indexes. So the parameters in order will go `value`, `value` again (which you can actually just put an underscore `_`, and then the `map`.
  
- The `map()` method is similar to the forEach method, but map method will take an array, loop over it and applies a callback function to the current array element. It will then 'map' these values into a new array - usually way more useful than the forEach method (no side-effects). The callback function will get the current element in the arguments (similar to forEach method). 
- The `filter()` method is used to filter elements in an array that fits a certain condition. It will return a new array that pass this specified test condition. These also get access to the element, current index and array. 
- The `reduce()` method boils/reduces down all array elements to one single value (i.e. adding all elements together). The reduce element also gets a call back function. THe first parameter is always the accumulator (acc - it's like a snowball, followed by the current element, then the index, then the entire array. It also has another SECOND parameter (which is the initial value of the accumulator in the first loop iteration - i.e. like saying let i = 0). CHECK USEFUL SCREENSHOTS IF UNSURE. Always know what the accumulator should be - this is quite challenging but very beneficial to use.
- You can also make the accumulator an object!! 
  
- It's usually good practice not to mutate arrays.
- The `find()` method retrieves an element of an array. It does not return a new array, but only returns the first element that satisfies a specific condition (if it is true or false). It is similar to the `filter()` method, apart from TWO BIG differences: filter will return all of the elements that match the condition, but find will only return the first one. The find method does not return a new array, it only returns the element/object itself (not the array). This is usally combined with the `===` operator.
- The `findIndex()` method is similar to the `find()` method, where you need to pass in through a condition (true or false). It will then return the first INDEX in the array that returns true (similar to the indexOf method - but with findIndex() we can create a complex condition - anything that returns true or false).
- The `findLast()` and `findLastIndex()` can be also be used similarly to get the last element or index, which can be good for using for 'latest transactions' or viewing the most recent activity.
  
- The `some()` method can be used (similar to the `.includes()` method) if you want to check if any item/element fits a particular condition. The difference is that the `includes()` method checks for equality, whereas the `.some()` method checks for conditions. Whenever you see the word 'any' included in questions or challenges, it's usually a good idea to use the `some()` method. 
- The `every()` method only returns true if ALL of the elements in the array 'pass the test' will be true.
  
- The `flat()` method creates a new array with all sub-array elements concactenated together. Useful for nested arrays and combining them into one to "flatten" the array. This only goes one level deep though. This also doesn't need a callback function. If it is one level deep of nesting, you would just use the `flat()`, but if it is 2 for example then you would just use `flat(2)`.
- The `flatMap()` method is used when you want to Map something and flatten it, however it only goes 1 level deep, no matter what, otherwise you will have to use the `flat()` method. This requires a call back function.

- To <strong>sort</strong> array's from A-Z (by default), you can use the `.sort()` method, bearing in mind that this will mutate the array. The sort method only does this on strings(by default). Numbers will be converted into strings first. To fix this, you can use a callback function in the sort() using the compare function (parameters of a, b). Have a look at useful screenshots, quite difficult to understand here. If you have a mix with numbers/strings in an array, DON'T use the sort method.
- <strong>Array grouping</strong> - occurs by `const elementName = Object.groupBy(array callback function(condition inside))`. This will loop over the array, and again can use the shorthand arrow callback function.

- To create an empty array, you can use the empty array method - `const x = new Array(7)` to create 7 blank arrays. 
- The `fill()` method will fill an entire array (and mutate the array). It is similar to the slice()method as we can tell it where we want to start it (begin parameter) and finish it (end parameter).
- The `Array.from()` tool will create a new array from an array like object or an iterable (set/map/strings/querySelectors). This syntax would be - Array.from(arrayLike, mapFunction, Argument) - the callBack function is optional.

- REMEMBER: The `reverse()`, `sort()` and `splice` method, - will mutate arrays (which usually isn't good practice). These are <strong>DESTRUCTIVE</strong> methods. These can be replaced by `toReversed()`, `toSorted()`, and `toSpliced()`. 

- The `with()` method receives two arguments (the index, and new value). I.e. `const newMovements = movements.with(1, 2000);` would mean that the `1` is the index, and the `2000` is the new value. This can help to update a number of a new array, with the original array staying the same.

- <strong> CHOOSING WHICH ARRAY METHOD TO USE: </strong>
- Check useful screenshots for big list of when to use what! 
- The most straight forward method is the `.map()` method if it has the exact same length as the old one.
- If we want to filter for a condition - `.filter()`
- If we want a portion of the original - `.slice()`
- If we want to replace an item - `width`
- The methods 'that should be avoided these days' are the following, as they all mutate the original array:
<ol>
  <li>.push()</li>
  <li>.unshift()</li>
  <li>.pop()</li>
  <li>.shift()</li>
  <li>.splice() - we would use `.toSpliced` </li>
  <li>.reverse() - we would use `.toReversed` </li>
  <li>.sort() - would use `.toSorted` </li> - for toSorted - have a look at the useful screenshots folder! especially for the compared function.
  <li>.fill()</li>
</ol>

- The prefix `++y` operator will increment the variable before using, whereas the `y++` operator will increment that variable after using it.

### Numbers Advanced
- Numbers are always displayed in JS as decimals. Numbers are also only composed in a binary format (0 and 1's).
- You shouldn't do really precise scientific or precise financial programs in JS due to the errors.
- <strong>Parsing</strong> - can change a number to a string - i.e.
- `Number.parseInt` - will display the integer - it's important, for the second value to always put 10 to avoid bugs as JS works with 'base 10 - which are numbers 0-91'. 
  `console.log(Number.parseInt('30px', 10)) ---> 30` - this would equal 30 in the console. But in order to use this you have to ensure that the value starts with a number.
- You also have `Number.parseFloat` which can be ideal for decimals and should be a go to when you want to read a value out of a string (mainly from CSS). 
- You don't have to call these on the Number object, but it is actually better practice, as it provides a namespace for the function.
- The `Number.isNaN` - can help to check if most values are a number (in a boolean). It checks if it is NOT a number. It is not the best way to check if things are not a number. We rarely use this. A better method is -
- `Number.isFinite`, as it checks if it IS a number or not - this is way more understandable for me.

<strong>Mathematical Equations - the math name space</strong>

- The `Math.sqrt()` can give us the square root of a number.
- The `Math.trunc()` can remove decimals. Math.floor is better as it can work better with positive and negative numbers/strings.
- The `Math.round()` can also round to the nearest integer.
- The `Math.ceil()` will round UP and `Math.floor()` rounds down. `Math.floor` is better as it can work better with positive and negative numbers/strings.
- The `Math.max()` can return the maximum value to us - this will do type coercion. It does not do parsing though, it will return NaN. The `Math.min()` is the same, but the opposite.
- Math.random will generate are random number (between 0 and 0.9999).
- Rememember that Math.random() does not take in arguments!!
- `const randomInt = (min, max) => Math.random() * (max - min + 1) + min;` - this is your random number generator!! 
- When rounding decimals, you will need to use the `().toFixed()` method. toFixed will always return a string however. The end bracket on the `().toFixed(2)` will add two decimal places. To convert it to a number, you then just use the `+` in front.

- <strong>The remainder/modulo operator `%` </strong> - is the remainder of a number after being divided (way easier to remember than how it was explained in my last course).
- Example 1: `8 % 3` - you would think, how many times does 3 go into 8 `3 x 2 = 6` the remainder of this is `2`.
- Example 2: `10 % 3` - 3 goes into 10 3 times = `9`, remainder of `1`.
- In order to check if a number is even/odd - check below:
- <strong> EVEN NUMBER </strong> - `const isEven = n => n % 2 === 0;`

- In order to make numbers easier to read in code, place the underscore in it, as JS doesn't pick it up - i.e. `36_000` would be `36000` in the console (`this is a numeric seperator`). Just can't be at the beginning or end of a number, and can't place 2 in a row. This also doesn't work for strings.
- The `Number.MAX_SAFE_INTEGER` was the biggest number that JS could handle (check console.loog) until `bigInt` came along.
- If you have a number that is very large, but an `n` on the end of it, which will transform it into a bigInt. This changes the colour in the console to grey also.
- You can also use the `bigInt()` function without the `n` which will do the same thing, but for smaller numbers.
- It is not possible to mix bigInt() numbers with regular numbers in mathematical equations and name spaces (like Math). But you can do `<` and `>` and `==`.

- <strong>Dates</strong> - to create the data currently, you would use the `new Data();` which would give you the current day/year/time.
- Months in JS are zero based, so starting at 0 - meaning June would be 7, December would be 13 etc.
- Dates have their own methods, as they are objects.
- Parameters - `new Date(year, month, day, hours, minutes, seconds)`
- Look at useful screenshots folder for all of the relevant information for dates.
- Have a look at the `Intl.DateTimeFormat` and `Intl.NumberFormat`

- <strong>TIMERS</strong>
- `setTimeout()` receives a callback function. The first argument is the callback function, and the second argument is the amount of ms that will pass until the function is called i.e. 3s would be 3000.
- As soon as JS hits the setTimeout() function line of code, it will keep counting the time in the background, and register the callback function after the time has elapsed. JS will then move onto the next line. This is called <strong>Asynchronus JavaScript</strong>.
- All the arguments that you pass after the delay, will be arguments after the function.
- The `clearTimeout` function can be used with a condition - check useful screenshots.
- The `setInterval` can be a great way of displaying the current day and time/seconds on your website. See an example below:
- `setInterval(function () {const now = new Date(); console.log(now);}, 1000);` which would set up an interval every second, like changing the time every second on the web page.
- The `clearInterval` can be done to do the same as clearTimeout, but with the setInterval function.
- It can be quite important to put a timer in the global scope, so it is able to be accessed from everywhere - just for ease.

- ### WEB DEVELOPMENT FOR JS!! - ADVANCED DOM

- When there is an href, the page will automatically jump to the top when it's clicked (default behaviour - which doesn't look very nice). To revert the default you can use the `e.preventDefault()` in the function.

- <strong>Selecting, deleting and creating elements</strong>

- <strong> Selecting elements</strong> 
- To select the entire html, use `document.documentElement`, for the head would be `document.head` and body `doucment.body`. We dont need to write the `selector` here.
- You can have `document.getElementByID()`, `document.getElementByTagName()` - the getElementByTagName won't return a node list, instead it returns an html collection (live collection - meaning if the DOM changes, the html collection will update automatically). The same doesn't happen for a node list. You can also have `document.getElementByClassName()`. You don't need a dot here, cause you are already specifying the class, and this will also bring back an html collection. 
- `document.querySelector` and `document.querySelectorAll` are the most common.

- <strong>Creating and inserting elements</strong>
- The `.insertAdjacentHTML()` is probably the most common use for creating. You will need to add this on the parent element. 
- The `const = variableName = document.createElement('div')` for example, will create an element, and store it in the message (it is just a DOM object that we can use). If we want it on the page we need to insert it. You can then use this variableName and do things with it - i.e. `variableName.classList.add()`. 
- To insert it for example, `header.prepend(variableName);` - the prepend() inserts the element into the HTML/DOM - it adds it as the first child of the header element for example. The `header.append(variableName)` will do the same, but it will be the last child of the header for example. It can't be put in both places (can't be at the same place at the same time).
- You can also insert it before `header.before` - this will be a sibling element, before the header, and after (same concept).

- <strong>Delete elements</strong>
- All you have to do is add `variableName.remove()` in the callback function of the eventListener (after querySelector).

- <strong>STYLES</strong>
- I.e. `variableName.style.backgroundColor = '#37383d'`.
- When styling in JS, most of the styles will become inline styles.
- In order to see the styles (that aren't inline styles), you can use the `console.log(getComputedStyle(variableName).color)` for example.
- In order to change styles for example, you can use the `document.documentElement.style.setProperty('--primary-color', 'orangered')`. This would change the primary color to orangered. You can do this with any property. 

-  <strong>ATTRIBUTES</strong>
- For example - `const logo = document.querySelector('.nav__logo')` and then you can `console.log(logo.src)` or `console.log(logo.alt)'` or `console.log(logo.className)` to find out what these values are.
- You can also set these e.g. - `logo.alt = 'cool alt'` which should change the text of the logo alt.
- The `variableName.setAttribute('', '')` and `variableName.getAttribute('')` can also be used.
- To see the current viewport - `console.log(document.documentElement.clientHeight, document.documentElement.clientWidth)`. 
- <strong>CLASSES</strong>
- Just really need to know the following - `classList.add()`, `classList.remove()`, `classList.toggle()`, and `classList.contains()`.

- <strong>SMOOTH SCROLLING OLD SCHOOL</strong>
- The `const s1coords.getBoundingClientRect()` returns an object rectangle (the s1coords is are the coordinates providing information about the size of an element and its position relative to the viewport.
- The `console.log(e.target.getBoundingClientRect());` - `e` is the event object automatically passed into the function when an event (like a click) happens.
`e.target` refers to the actual DOM element that was clicked. `.getBoundingClientRect()` is a method that returns the position and size of that element relative to the viewport (not the entire document).
-  `console.log('Current scroll (X/Y)', window.scrollX, window.scrollY);` - doing this you can see where the coordinates from where you have scrolled in the viewport, from the original point. Obviously x is from left-right, y is from top-bottom.
- You use window.scrollTo(param1, param2) which is a global function. The first parameter is the left position (which is usually 0 but find it out from the `getBoundingClientRect()` information - we want it to be 0 because we don't want any horizontal scroll. The second parameter is the top position, from the top of the viewport.
- Example - `window.scrollTo(s1coords.left, s1coords.top);`.
- It is quite challenging to get it perfectly right with the top numbers, so you can add values to the numbers depending on how the smooth scrolling looks.
- In order to find the absolute positioning of an element, relative the document do the following:
- `window.scrollTo(variableName.left + window.scrollX, variableName.top + window.scrollY)`.
- In order to make the scroll 'smooth' - do the following:
- `window.scrollTo({
    left: s1coords.left + window.scrollX,
    top: s1coords.top + window.scrollY,
    behavior: 'smooth',)`

- <strong>SMOOTH SCROLLING NEW SCHOOL</strong>
- Only works for new browsers, but should be okay for most things
- Instead of the code above - you would use - `section1.scrollIntoView({behavior: 'smooth'});` - so much easier.
- Still important to know the one above though.

- <strong>MORE EVENT LISTENERS</strong>
- The `mouseenter` event can be used on the addEventListener where the 'click' event is usually. It fires whever the mouse enters a certain element. This is similar to the hover for CSS. This is better as we can add chains on top, and we can remove an eventhandler, in case we do not need it anymore.
- Just important to know that `mouseenter` does not bubble. 
- In order to be able to only listen to an event once, a good idea is to use the `removeEventListener()` function i.e. `removeEventListener(mouseenter, variableName)`
- The `onmouseenter` property can be used directly on the element, rather than the eventlistener. We mainly use
- <strong>Capturing Phase</strong> - The capturing phase does not actually occur where the event is clicked (for example), it actually starts at the top/root of the document, and makes its way down to the target element (down the tree), passing through every single PARENT (not sibling) element. As soon as it reaches the target, the target phase begins.
- <strong>Target Phase</strong> - occurs where the callback function starts to occur, which will start the event.
- <strong>Bubbling phase</strong> - this event then travels/bubbles its way back up to the root of the document. It's as if the event is occuring in each parent element. 
- In any event handler, the `this` keyword and the `e.currentTarget` will always be the same.
- In order to stop propogation into the parent elements, you can use `e.stopPropagation()` function. BUT THIS IS NOT RECOMMENDED - only if you are coming up with a few bugs.
- The `addEventListeners` are only listening for events in the bubbling phase, not the capturing phase. This is due to the capturing phase not really being that important to us.
- The `e.target` is the reference onto the object on which the event was dispatched. It is different to `e.currentTarget` when the event handler is called during the bubbling or capturing phase of the event.

- <strong>Event delegation</strong> - We need to attach the event handler on the common parent element of all the elements we are interested in. It requires 2 steps:
<ol>
  <li>Add the event listener to a common parent element.</li> 
  <li>Determine what element orignated the event `(console.log(e.target))`.</li>
</ol>
- You can then use the matching strategy, to ensure that any elements that are not needed in the event handler are not included in the event. See below and in useful screenshot folder.
- `if (e.target.classList.contains('variableName') console.log('link')}`

- <strong>DOM traversing</strong>
- <strong>Going downwards - child elements</strong> - `element.querySelector`, `element.querySelectorAll`, `element.children` - to see the direct child element, `element.firstElementChild`, `element.lastElementChild`.
- <strong>Going upwards - parent elements</strong> - You can use the `element.parentElement`. The `closest()` method can tell us which is the closest parent of a particular element (i.e. `h1.closest(.header)` - so which is the closest parent class of `.header` to the `h1`. It will receive a query string, just like the query selector method. Inside the paranthesis you will put a class or ID - and it is the closest parent to that particular class/ID. You can think of the closest() method being the opposite of the querySelector - querySelector finds children (no matter how far down in the DOM tree), and closest will find parents (no matter how far up).
- <strong>Going sideways - siblings</strong> - You can use the `element.previousElementSlibling` and `element.nextElementSibling`. You can also do `element.parentElement.children` to get all of the element's siblings, including itself. 
- You can also do the above to check all of the nodes, but not really necessary.

- A guard clause - is an if statement that will return early, if a condition is matched (good use for when you want to immediately finish a function). It usually checks for the opposite of what we are interested in - and if it returns back true, it will finish the function.
- I.e. `if (!Number.isFinite(distance)) return alert('Inputs have to be positive numbers!')`

- Intersection Observer API - allows us to observe changes to the way a certain target element intersects another element or the viewport.
- All sections of the DOM will be observed when the page is loaded.
- Have a look at useful screenshots for this.
- You can use the `.length` property on Nodelists too.

- <strong>Efficient script loading</strong> - 
- Using `defer` in the head, is overall the best solution to ensure that the scripts are executed in order. I.e. `<script defer src="script.js"></script>` in the head section. 

### Object Oriented Programming 

- Classes are used in objects to act as a blueprint. From this class, you can have multiple `instances/objects` which is the data inside of the class.
- There are 4 fundamental principles of OOP -

<ol>
  <li>Abstraction - To ignore/hide details that don't matter, allowing us to get an overview perspective of the thing we are implementing. We are pretty much just removing the low-level details.</li>
  <li>Encapsulation - Keeping some properties and methods private inside of the class (not accessible from outside of the class). Some methods can be exposed as a public interface (API).This prevents external code from accidentally manipulating internal properties/state (to avoid bugs).</li>
  <li>Inheritance - Makes all properties and methods of a certain class available to a child class. This allows us to use common logic.</li>
  <li>Polymorphism - A child class can overwrite a method it inherited from a parent class.</li>
</ol>

- Each object will have a `prototype`. Protytpal inheritance means that all objects that are linked to a certain prototype object can inherit methods/properties. A prototype contains methods and an object can access methods.
- Array.prototype is the prototype of all array objects we create in JavaScript. Therefore all arrays have access to the map method.
- There are 3 ways of implementing prototypal inheritance in javascript - these are constructor functions, ES6 classes (more modern way - not the classes I mentioned above) and Object.create() - which is the easiest and staright forward way, but not used as much.

- A constructor function is a normal function (only difference is that we call the constructor function with the `new` operator. Constructor functions always start with a capital letter. Arrow functions do not classify as a constructor function (as it doesn't have its own this keyword). In a regular function call, the 'this' keyword is undefined. 
- Never create a method inside of a constructor function. This is where you want to store all of the code that is executed right when the application loads. 

- <strong>Prototypal inheritance/delegation</strong>
  
// 1. New {} is created
// 2. function is called - and an empty object is created. The 'this' keyword is set to the eenew empty object.
// 3. The new {} object is linked to the constructor function's prototype property (__proto__property). This happens internally and the `__proto` always points to the object's prototype. 
// 4. Function automatically returns the new object {} from the construction function call. 
These 4 steps work for the ES6 classes and constructor functions, but not `Object.create()`. If a property or a method cannot be found in a certain object, JS will look at it's prototype. 

- `Variablename.prototype` - prototype is not the prototype of person, but it is the prototype of all of the objects created by the variable name. 
- All objects in JS will have their own prototype. At the top of the prototype chain is usually `Object.prototype` which usually has a property of `null`. The prototype is very similar to the scope chain.

### ES6 CLASSES - check useful screenshots for some examples

- classes are a special type of function (you can have class expressions and class declarations).
  
- Class expression - `const variableNameCl = class {}`.
- Class declaration - `class variableNameCl {constructor(paramaters)}`.

- Remember that classes are not hoisted. Classes are first class citizens (as they are special kind of functions). Classes are always executed in strict mode
- You can write methods inside of the class (outside of the constructor), but these will be on the prototype of the objects, and not on the objects themselves. This is like prototypal inheritance (- The methods will be added to the .prototype property)
- In constructor functions, you can have as many `this.variableNames` as you want, they don't even need to be included in the inputs. 

- Only use classes if you understand prototypes and prototypal inheritence. But if you want to be confident, you need to understand all of this.

- <strong>Getters & Setters</strong> - functions that get and set a value.
- Any setter has to have one parameter in the parenthesis.
- Getters and setters behave like properties, not functions - so you don't need to call these like a function call.
- In a setter, you are trying to update the property on the obejct. The setter’s job is to take the input, transform it, and update the object’s internal state.
- These can be very useful for data validation. 
- Check useful screenshots for a good way of looking at it.

- <strong>Static methods</strong> - these methods will not be inherited. These are not available on instances. You would use the static method here.

### Object.create()

- There is still the idea of prototypal inheritence. However, there are no prototype properties, no constructor functions and no `new` operator. 
- We can use Object.create() to manually set the prototype to any other object that we want. This is different from constructor functions, as this is done automatically. 
- The big difference is that we didn't need any prototype properties or constructors. The prototype chain still will look the same - this is usually quite straight forward compared to the other ways. This is the least used way however - still important to know.
- The big takeaway is that `object.create()` creates a new object, and the prototype of that object will be the object that we pass in. 

- <strong>Inheritance Between Classes: Constructor Function</strong>

- Usually we want a child class to have the same functionality as the parent class with some additional functionality (usually we pass in the same parameters + some additional ones).
- Check useful screenshots for inheritance between classes (as has some notes too).

- <strong>Inheritance Between Classes: ES6 Classes </strong>

- For this we only need two ingredients, the `extend` keyword and the `super function`.
- The `extend` keyword will link the prototypes behind the scenes.
- Again check useful screenshots.
- If you don't need any new properties, you will not need a constructor method in the child class! 

- <strong>Inheritance Between Classes: Object.create()</strong>
- Check useful screenshots - not really used as much - mainly use ES6 classes (which is unfortunate as I find this easier to understand).

### Encapsulation (Privacy) 

- This is an important feature of object oriented programming. Encapsulation is to keep some properties/methods inside the class private (so they are not accessible outside of the class). We can then expose these methods to the public interface (API). We call this whole idea <strong>DATA PRIVACY</strong>.
- This is to prevent code from outside of a certain class to manipulate data inside.
- Properties in OOP are called fields. With class fields, classes now start to have abilities that we didn't have previously. A field is a property that will be on all of the class instances (we also call this a public instance field). These fields will not get inherited.

<ol>
  <li>Public Fields - to declare a field, you do need semi-colons and no this keyword + no const/let. Just the name of the field and a value i.e. `locale = navigator language;`. This will then be on every single instance, but not in the prototype chain.</li>
  <li>Private Fields - Same as the public fields in terms of layout, but you would start with `#variableName = something`. Private means that the data cannot be accessed/mutated outside of the class.</li>
  <li>Public methods</li>
  <li>Private methods - to convert public method to private method just do the `#` infront of the methodd name.</li>
  <li>Then a static version of all of these! - these are usually a lot less important. Static fields are not inherited on the prototype, they are only accessible on the class themselves (not on the object).</li>
</ol>

- We can chain methods in classes. This is common in OOP in JS. In order to do this, you just need to return `this` for each of the methods you are wanting to chain.
- Check print out for summary + extra notes.

- Geolocation Navigator (API) - `navigator.geolocation.getCurrentPosition()` - takes 2 call back functions. The first function is the callback that works on 'success' - whenever the browsers get the coordinates of the user. The second function is the callback that works on an 'error' while getting the coordinates.
- On forms, the default behaviour once things are submitted is to refresh the page, so just set the `e.preventDefault()` if using JS for forms.
- An event handler function will always have the 'this' keyword of the DOM element of for which it is attached - i.e. `form.addEventListener('submit', this._newWorkout)` - would be `form`. To fix this you always use `bind()` as you want to point the this keyword to the object.
- Any object should have some kind of unique identifier, so that later we can identify it through its ID - we would have to use an ID library usually.
- It's a good habit to use 'small helper functions' to make your code a lot cleaner. 

- <strong>Working with local storage</strong> - this is an API - `localStorage.setItem('name', 'string you want to store and be associated with a key')` - it is only advised to use for small amounts of data otherwise it will slow down the application. If you open up the console, go to application and have a look at local storage, you can see the results.
- You can also use `.getItem`
- `JSON.stringify()` - is how you can turn anything into a string. The opposite of this is `JSON.parse()` - I don't think stringify can return private variables.

### Asynchronous JS, AJAX & API's 

- Most code is synchornous (code executed line by line where each line of code waits for the previous line to finish). Asynchronous code (take a setTimeout function for example) is executed after a task that runs in the background finishes (so the main code is not blocked and execution doesn't wait for an asynchronous task to finish its work). Call back functions and event listeners alone, do not make javascript asynchronus though.
- Setting a src of an image is actually asynchronus as it is loading the image in the "background".
- <strong>AJAX</strong> - Asynchronus Javascript And XML - allows us to communcate with remote web servers in an asynchronus way. With AJAX calls, we can request data from web servers dynamically.
- Online API - an application running on a serve that receives requests for data and sends data back as a response - we just call these Web API's or API.
- `XML` is a data format that we don't really use any more. We use the `JSON` data format more - which is the most common (a data object just converted into a string making it easier to use).
- Asynchronus tasks only run in the WEB API's environment of the browser. If it was synchronous, it would be happening in the callstack. That is why loading images is asynchronous. 

- Old school way of doing AJAX in JS - `const request = new XMLHttpRequest(); ` - check useful screenshots folder for whole code.
- `Callback hell` - when we have a lot of nested call backs - noticed by a lot of indentations on lines. This makes our code look very messy and hard to maintain/understand. This leads to more bugs.
- A way to escape callback hell is by using 'promises'.
- A `promise` is an object used as a placeholder for a future result of an asynchronous operation (container for a future value - i.e. a response from AJAX call). The big advantage of using promises is that we no longer need to rely on event and callback functions to handle asynchronous results. Also allows us to escape callback hell to avoid the nesting of callbacks.
- `Promises` are time sensitive. At the beginning, the promise is pending (before the future value is available), when the asynchronous task is finished (settled), they can either be fulfilled promises (successfully resulted in a value) or rejected promises (there has been an error during the asynchronous task).

- The new way of doing AJAX is using the `fetch()` method. Inside will be the url of the API.
- The fetch method can also have the `.then(function(response){})` method which will need to include a callback function to use as soon as the promise is fulfilled. Check useful screenshots for full code.
- The `.json()` method is available on all of the `response/res` parameters of the fetch method. This will also return a new promise as it is an asynchronous function.
- Async functions will only return promises. You can use the `.json()` method on top of the 
- The fulfilled result of the promise will always be the value that we return from the `then()` method.
- To handle rejected promises (such as losing an internet connection). The first way to handle a rejected promise is to add a `catch()` method at the end of the chain. i.e. `.then(data => renderCountry(data, 'neighbour')).catch(err => alert(err))`.
- The `finally()` method is a callback function that can be useful (i.e. hiding a loading spinner when an asynchronous item starts)
- You can also manually throw an error. For example - please see important screenshots.
- Handling errors is the only way we can display error messages on the screen for the user - it is bad practice.

- The `event loop` looks into the call stack and determines whether it's empty or not (except for the global execution context). If it is empty, it will take the first callback of the callback queue to put into the execution context to be executed. This is called an event loop tick ✅. It basically coordinates when each callback is executed. 
- Promises work a little differently. Callbacks that come from a promise will not be moved into the callback queue. They have a `microtasks queue` which has `priority` over the callback queue. It will run all of the microtasks queue before the callback queue (doesn't matter if it is empty or not).

- INTERVIEW QUESTION: HOW CAN ASYNCHRONOUS CODE BE EXECUTED IN A NON-BLOCKING WAY, IF THERE IS ONLY ONE THREAD OF EXECUTION IN THE ENGINE? -
- THE WEB API'S, CALL STACK, AND CALLBACK QUEUE ALL WORK TOGETHER IN A NON-BLOCKING WAY, EVEN THOUGH THERE IS ONLY ONE THREAD OF EXECUTION IN THE ENGINE - good to explain how they all relate together.

- To create a new promise - `const variableName = new Promise(resolve, reject) {})` - it takes one argument which is an executing function (to automatically execute the executing function).
- In practice, most of the time we just consume promises. We only build promises 'promisifying' - to wrap old callback based functions into functions. 
- The executing function will contain the asynchronous behaviour we are trying to handle with the function - the future value of the promise).
- The `resolve()` part of the executing function will set the promise as `fulfilled/resolved`. You would pass the fulfilled value of the promise here, and then match it with the `then()` method/handler.
- The `reject()` function of the executing function will set the promise as an error message, that we would later want available in the `catch()` method. 
- You would then 'consume' the promise (check out useful screenshots folder).

- An easier way to consume promises - is to create an `async` function - i.e. `const whereAmI = async function (country) {}`. This will mean that the function will keep running in the background while performing the code that is inside of it.
- We can have 1 or more `await` statements - which will 'await' for the result of the promise (i.e using the fetch() method). This await will not stop the call stack (this is what is so special, it makes it look like synchronous code, but will actually be asynchronous code). We can then assign this value to a variable (which we can't do while using the `then()` method).  Check useful screenshots.
- It is probably better to use `await` statements. They can only be used inside of an `async` function or an async IIFE.
- In ES6 we can now use await statements outside of async functions (in modules). 


- `try...catch` is a way to handle errors in JavaScript without crashing your whole program - it allows you to try some code that might throw an error - see below: - we always should wrap `async` functions in `try... catch` blocks. 
  
  `try {
  let result = someFunctionThatMightFail(); // This might throw an error
  console.log(result); // Won't run if the above throws
} catch (err) {
  console.log("Something went wrong!");
  console.log(err.message); // Shows what the error was
}`

- `Promise.all()` function takes in an array of promises, to return a new promise. To run all of the promises in the array at the same time (able to run in parallel). If one promise rejects here, then all of the promises will reject. 
- Whenever you have to do multiple asynchronous operations at the same time (that don't depend on one another) always run them in parallel in `Promise.all()`.
- `Promise.race()` function takes in an array of promises to return a new promise BUT it will be settled as soon as one of the input promises is settled (or is available) - the first settled promise wins the race. A promise that gets rejected can also win the race. `Promise.race()` is very useful to prevent against never ending promises, or long running promises. Check useful screenshots folder.
- `Promise.race()` and `promise.all()` are the most important to know.
- `Promise.allSettled()` will take in an array of promises, and will simply return an array of all of the settled promises (similar to promise.all() but promise.allSettled() will return all of the results).
- Promise.any() takes an array of multiple promises and will return the first fulfilled promise (ignoring the rejected promise - will always be a fulfilled promise).

### Modern JavaScript Development 

### Modules
- Modules are reusable pieces of code that encapsulates implementation details (they make it very easy to compose software). Modules are a great way to isolate components too (can be developed in isolation without thinking about the entire codebase). They can also abstract code and make code easier to understand (more resuable code and organised code).
- Modules involve importing (dependency) and exporting (public API). Imports and exports can only occur in the top level. All imports are also hoisted. Importing values is always the first thing that occurs in the module 
- <strong>Differences between old school scripts and ES6 modules</strong> - In modules, all top level code are scoped to the module. The only way an outside module can access a value that's inside of a module is by exporting the value. In scripts, all top level variables are always global. ES6 modules are always in strict mode (by default), the top-level `this` keyword is undefined (whereas in script it is the `window` object), and file downloading always occurs in an asynchronous way for ES6 modules. 
- To link the module to the html file - `<script type="module">`. We also usually list all of the imports at the start of the file. 
  
- <strong>How ES6 modules are imported</strong> -
  
<ol>
  <li>Parsing occurs (reading of the code) - this is the part where imports are hoisted (even before the code is executed). Modules are imported synchronously (only after all imported modules have been downloaded and executed, the main index.js module will be executed) which makes the imports known before their execution (doing this synchronously makes bundling and dead code elimination possible).</li>
  <li>Modules are then downloaded from the server in an asynchronous way (they are also parsed and the modules exports are linked/connected to the imports in the index.js module).</li>
  <li>The code in the imported module is executed (and process of importing is finished).</li>
</ol>

- By default, all top level variables are private inside of the current module (unlike traditional scripts). If you wanted to use them, then you would have to use exports (named exports and default exports).
- To change the name of some exports you can do `totalPrice as price` for example - this would change totalPrice name to price.
- To import everything you can use `import * as` which will import everything from the module that you declare.
- `Default exports` are used only when we want to explore one thing per module. This would take in a 'value'. You would use `export default`. To import it, you would use `import add from ./path.js`
- We never mix named and default exports in the same module
- IMPORTANT - imports are not copies of the exports (they are a live connection - pointing to the same place in memory).

- <strong>Top level await</strong> - only works in modules. You can do this outside of an async function. While this is useful, it actually blocks the execution of the entire module now (which is sometimes not what we want) - use this with great care. 
- If one module imports a module with a top level await, then the importing module will wait for the imported module to finish the blocking code. 

- All modules in the NPM (code sharing) use the common JS module system (so it is still very important to know). Check useful screenshots for importing/exporting in Node.JS.

- <strong>The command line</strong> - terminal inside of VS code.
- The `ls` keyword will show all of the files.
- The `cd` keyword will change directory (to go up and down the file tree). To go up one tree `..`, to go up two levels - `../..`.
- The `clear` would obviously clear the terminal.
- To create a new folder - `mkdir FOLDER NAME`.
- To go into the new folder - `cd FOLDER NAME`.
- To create a new file - `touch FILE NAME`.
- To remove a new file - `rm FILE NAME`. To remove an empty folder - `rmdir FOLDER NAME`. To remove an entire file - `rm -R FOLDER NAME`. 
- To move a file in the terminal - `mv FILENAME ../` for example.

<strong>Using NPM</strong>
- using NPM in the terminal to create `package.json` which is a file that will store the entire configuration of your project. Start with the new terminal - `npm init`.
- We can't use common JS modules without a module bundler.
- Never include the node modules folder when copying your project folder to somewhere else (because it is too huge).

- Install `npm i parcel@2` for version 2 of parcel in the terminal after editing the package.json files. - adding under "scripts": - `"start"` and `"build"`.
- To run the start of the script - `npm start` - which will call the 'start script'
- Bundling using <strong>PARCEL</strong>: `npm i parcel --save-dev`.
- `npx` is an application built into npm. `npx parcel index.html`.
- Have a look at proper bundling on lecture 290 as quite confusing. Parcel can also translate CSS into SASS (which is a better way to store CSS for big projects). 

- Using <strong>Babel</strong> for ES5 - Parcel automatically uses it. Babel can only compile ES6 syntax.
- We can polyfill these new features in our code. Babel used to do it, but now we have to manually import a new library - `import 'core-js/stable';` in the script or `npm i core-js`. This would import everything so leading to a large bundle size, otherwise you can do - `import 'core-js/stable/array/find';` if you are looking for the find() array method for example - but we usually don't do this.
- To polyfill async functions - `import 'regenerator-runtime/runtime';` and `npm i regenerator-runtime`

- <strong>Declarative vs Imperative Code</strong>
- <strong>Imperative code/programming</strong>: is like us explaining to the computer HOW to do things - every single step it has to take to achieve a result (like a baker following instructions on how to make a cake).
- <strong>Declarative code/programming</strong>: is like us telling the computer WHAT to do - the how (step-by-step instructions) gets abstracted away (like describing what the cake looks like). This has given rise to <strong>functional programming</strong> - writing software by combining many pure functions and avoiding side effects/mutating data.
- Some examples of declarative syntax include - array and object destructuring, the spread(...) operator, ternary/conditional operators and template literals. 
- <strong>Side effects</strong> are modifications/mutations outside of the function (mutating external variables, logging to console, writing to DOM etc).
- <strong>Pure functions</strong> are functions without side effects and does not depend on any external variables.
- <strong>Immutability</strong> - means that the state/data is never modified (instead the state is then copied, and it is the copy of the original state that is mutated). This makes it easier to keep track of code and write better code without bugs.

- `Object.freeze()` can freeze objects and arrays to make them immutable. Object.freeze() only 'freezes' the first level of the object (meaning we can still change values/properties - it just means we can't add new things to it). 
- 
