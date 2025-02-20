# JavaScript Notes from Angela Yu Course + Jonas Course

### Javascript (ES6) 

- ES is shorthand for ECMAScript (which is the european computer manufacturer's script).
- Java vs. Javascript - no relation whatsoever. Javascript is an interpreted programming language (meaning it kind of translates to the compiled language what to do - starts slowly and you can check how it is going during the process) whereas Java is a compiled programming language (meaning it does the job the interpreter has set out - starts quickly, but you can't really see what is happening throughout).
- Interpreted languages are languages such as Javascript, Python & Ruby - whereas compiled programming languages are like Java, C/C++, and Swift.
- When opening the JavaScript console, to write a double line of code, hold shift and press enter.
- Using the snippet editor of JavaScript console is a great way to write and test your code.
- `alert("Hello");` - the `alert` is the FUNCTION (gets the browser to do something), `"Hello"` is the MESSAGE that you want displayed (AKA the STRING) and the `;` is the END of the instruction so that the browser doesn't get confused between one line and the other.


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

- <strong>Strings</strong> can be combined using concantenation. `alert("Hello" + " " + "Name");` would mean that it would equate to "Hello Name" on the pop up section.
  
- You can easily find out the number of characters in a string by stating `word.length` `(variablename.length)`
- `var` is pretty much the same as using `let` - BUT there are many differences. 
  
- The <strong>Slice(x,y)</strong> function allows you to slice your strings to seperate them into individual characters. An example:
`var name = "James";`
`name.slice(0,1);` - would mean that the J is being selected. Programmers always start from 0, so although 'James' has 5 letters, S would be 4 (as J is 0). In order to grab the last letter though -
`name.slice(4,5);`

- `word.toUppercase()` - can turn every single character in a string to uppercase. Same with `word.toLower`

  
<strong>I am finding this super challenging...</strong>


- <strong>Numbers</strong> - you can add by `+`, subtract by `-`, division by `/`, multiply by `*`, but the <strong>modulo</strong> is represented by a `%` sign. The <strong>modulo</strong> will give you the remainder of the division (see below):
- You can do 'to the power of' by `**` i.e. `2 ** 3`. 
- `var a = 13 % 5; // 3` as this is the remainder of the 2 values when being divided by the number. 5 can go into 13, twice and then whatever is left is the number - i.e. 3. 
- another example: `var a = 16 % 4` would be 0, as there is nothing remaining.
  
- It is good programming practice to add a set of parantheses during BEDMAS protocols with numbers (even when you know this will happen by default).
  
- The <strong>Increment expression</strong> is another way of using `x = x+1` but you would use `x++` (which is the equivalent). `x = x-1` would be the same as `x--` and this would be the <strong>Decriment expression</strong>. You are only ever changing the value by one. If you need to increase by a specific number or variable, then you would use `x +=` and then by the number/variable, same with `x -=`. You can also do this for *, /, etc.
  
- <strong>Functions</strong> allow you to create a set of instructions and package it into a block of code `function getMilk() { }`. Function is the keyword (stating that we are about to create a new function), the getMilk is the function (to identify the new function), and then the instructions will go into the curly brackets.
  
- There is a difference for when you create the function and USING/CALLING the function. To do this you just would put `getMilk();` into the code. This means the computer will carry out all of the instructions into the curly braces.
- It is important to indent the lines of code inside of the curly braces (or the function's instructions) so that it is easy to tell they are the instructions in the code. <strong>THE CURLY BRACKETS DO NOT NEED TO BE CLOSED WITH A SEMI-COLON.</strong>

- <strong>console.log</strong> will log the string inside the console. The important difference between the alert and console.log is that the alert is something the user can see, whereas the console.log is not. This should be at the bottom.
  
- inputs within functions: `function getMilk(bottles) { }` - this "bottles" is used much like a variable (to contain the input) and you can use this inside of the function to do something with it. I.e. `function getMilk(bottles) { var cost = bottles * 1.5; }`. When calling, `getMilk(2)` then bottles would = 2. Cost of the bottle will then be 3.
  
- <strong>Floor Method</strong> is when you can ensure that a value is always rounded down to fit a "whole number" as opposed to 3.33 bottles of milk for example. You would need to do it like this: `var numberOfBottles = Math.floor (money - 1.5);`. The `Math.floor` if the floor function.
  
- There are also functions that are able to take an input and are able to use this inside the function to do something (or able to give an output).
- In order to get an OUTPUT out of the function, you need to use the `return` keyword. When we then CALL a function that has an output, we can use the output and assign it to a variable. This is usually added just before the closing brace i.e. `return money % 1.5;` which will give you the remainder of the division.
  
- <strong>Arrays</strong> are mutable components (meaning you can change the value of them using the index indirectly) `["first", "second", "third"]` that can hold a series of values (it is non-primitive data, meaning they can hold much more complex data - primitive data are numbers and strings which can only hold one value at a time).
- To access a value in your <strong>Array</strong>, you want to use the index (which means the first value will be `array[0]` which would mean 0 would be `"first"` for example.
- To get the last element in an array (as sometimes we do not know how many values are in an array), you can use the <strong>.length</strong> property via `array[array.length - 1] = 10 (or whatever value you want to change to)`.
  
- <strong>Methods</strong> are functions associated with certain values/objects (e.g. `.log()` is a method for the `console` object). Arrays have their own methods.
- `.push()` method is the first method associated with arrays and it allows you to "PUSH" or add a value to the end of an array. i.e. `arrays.push("value")` will add "value" at the end of your array. `.push()` will return the new length of the array, after adding the value you give it.
- `.pop()` method is the second method associated with arrays, and it allows you to remove the last element and returns this element back to you.
  
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

  
- `for` <strong>loops</strong> are used when you have to repeat a task multiple times. Loops need an <strong>iterator</strong>, which is a variable you can declare specifically in your loop to control how the loop iterates (or goes through logic). It is common to use `i` as your iterator variable. `for ("iterator"; "condition"; "iteration") {}`.
- `condition` tells the loop how many times it should iterate. When the condition becomes false, it will stop (BOOLEAN value = true/false).
- `<` is a less than operator which allows you to check if the value on the left is less than the value on the right. Usually an answer of true or false.
- `iteration` is a statement at the end which will tell the loop what to do after each run.
- Inside the body or curly brackets of the loop, should be the console.log(i) usually - take this with a grain of salt though until later in my learning.
- A `for...of` statement executes a loop that operates on a sequences of values from an iterable object (arrays and strings) and temporarily assigns it to a variable. `for (const value of iterable) {}`
- `\n` is an escape sequence/new line. THis is the old way of creating a new line, however you can now create a new line with back ticks, just by starting a new line in the code. 
