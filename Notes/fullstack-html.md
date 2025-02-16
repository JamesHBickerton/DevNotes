# Full-Stack Web Development Course Notes

## Table of Contents
1. [Frontend Development](#frontend-development)
    - [HTML](#html)
    - [CSS](#css)
    - [Bootstrap Framework](#bootstrap)
    - [Web Design](#webdesign)
    - [JavaScript](#javascript)
    - [Frontend Frameworks](#frontend-frameworks)
2. [Backend Development](#backend-development)
    - [Node.js](#nodejs)
    - [Express](#express)
3. [Databases](#databases)
    - [SQL](#sql)
    - [NoSQL](#nosql)
4. [APIs](#apis)
    - [REST](#rest)
    - [GraphQL](#graphql)
5. [Authentication](#authentication)
6. [DevOps & Deployment](#devops--deployment)
7. [Additional Resources](#additional-resources)

---

## Frontend Development

### HTML
- Notes on structure and semantics that I haven't included on my initial devnotes.
- `<hr />` and `<br />` elements are void elements. The hr will make a horizontal line and the br element will make a break in the line. But only use these sparingly due to accessibility issues.
- `../dog.png` will mean that the file directory needs to go further up the "file tree" whereas `./dog.png` means it will stay at the current directory/file path (the folder your png img is in). 


- Key elements and their uses

### CSS
- It is good practice to use the rem (root em) for font-size. This means the font-size will scale up in relation to the root (not the parent - which is the case for the em measurement).
- Borders go outwards, rather than inwards - so this doesn't change the width/height of an element.
- When adding border (similar to margin and padding - going clockwise around the element) - you need to use border-width, as border: 10px 20px 10px 20px will not work. 
- Pesticide (I have added to Chrome Extension) is a great way of seeing everything on screen so we can see div's, elements, alignment and sizing.
- Priority in order (from most to least) - ID, attribute ('li[draggable]'), class, element. 
- The `>` bracket can be used to select the DIRECT child element. selector > selector for example.

- The `selector (ancestor) selector (descendant) {` is a descendant selector - meaning that the descendant selector will be styled as the ancestor IF the ancestor is selected. This is many levels deep (so doesn't have to be the direct child) - but has to be within their enclosing brackets.
- Chaining selectors i.e. `selectorselector {` have no space between the selectors. If you have a bare element (i.e. h1) this will have to go before the class or id selector.


- <strong>Static positioning</strong> - default positioning - within the normal flow of a website.
- <strong>Relative positioning</strong> - item is positioned relative to it's default position (or relative from where it 'should' be).
- <strong>Absolute positioning</strong> - this will be positioned relative to it's nearest positioned ancestor (or the top left hand corner of the webpage). This is why you need to put `position: relative` on the nearest ancestor and `position: absolute` on the descendant so that the descendant is positioned in relation to the nearest ancestor.
- <strong>Fixed positioning</strong> - positioned to the top left window of the browser (stays in one place no matter how you are scrolling).


- `inline block` elements are a combination because you can set their height and width, but also can still be inline elements. For more info - https://appbrewery.github.io/css-display/
- Only use float if you want to wrap text around an image.
- You can use `display: inline-flex` so that the flex box components do not occupy all of the available space (this means that they will only take up whatever they need or whatever is displayed - i.e. flex-basis: 100px).
- `align-content` is similar to `align-items` but it only works if the `flex-wrap: wrap`
- If you set the `flex-basis` to a value, and the flex-item already has a set width, the `flex-basis` will override the `width` due to priority. This means it is a better idea to use `flex-basis`. `max width` and `min-width` would then ovverride the `flex-basis` due to priority too.
- Remember the shorthand flex: (grow) (shrink) (basis). `flex: 1` means that the grow and shrink are 1, and the basis is 0.
- Examples: https://appbrewery.github.io/flexbox-sizing-exercise/

- It is a better idea to use `1fr` for CSS grid as this will be more responsive moving forward.
- When you use the value `auto` on a row, it will fit to the content and if you use it on a column it will try to go to 100%. A good play around website would be the following: https://appbrewery.github.io/grid-sizing/
- You can also use `minmax(200px, 500px)` as a value for CSS grid-template-columns/rows. 
- Remember: `1fr` is a fractional unit.
- `grid-auto-rows` and `grid-auto-columns` you will need to look at how to do these properly.
- `grid-column` and `grid-row` are actually shorthand properties for `grid-column-start` and `grid-column-end`.
- `grid-area` is a combination (shows the coordinates for a grid item) for four values seperated by ` / `. The first is `grid-row-start` then `grid-column-start` then `grid-row-end` then `grid-column-end`. To use `grid-area` though, each grid-item will need to use `grid-area` too.
- `grid-template` is the short-hand for `grid-template-rows` & `grid-template-columns` in one line of code. You cant use the `repeat()` function here.
- In order to change the colours of the grid lines/gaps you need to just set the background colour to black/whatever colour you want.

### Bootstrap Framework (CSS) 

- Bootstrap is a type of CSS framework for more of a 'mobile first' approach. This has predefined CSS code and styling by using their components (designed by professional designers).
- This makes it easy and fast to use, with very consistent styling. You also don't really need to use media queries, as it is usually responsive. 
- The negatives of this is that it can create 'class bloat' meaning that all of the styling would be in the HTML, making it quite busy.
- It also makes it very hard to customise (making it hard to control).
- The best way to include this is using a CDN (content delivery network) in the `link` element in the `head` section your html.
- You also need the `script` to give the project functionality. This is pasted just before the closing tag of the body. 
- `getbootstrap.com` will have the CDN file.
- You need to make sure that the custom external stylesheet is BELOW the CDN link in the header (in order to override the bootstrap styling).
- This uses a 12 column system. Bootstrap has pre-defined breakpoints based on common screen sizes. XS would be for foldable phones, Small would be for mobile, medium for iPads, large for laptops, XL for desktops and XXL for TV's above.
- You can also have more than one breakpoint.
- https://appbrewery.github.io/bootstrap-layout/
- Spacing can be created by the bootstrap flow of: `{property}-(size)-(size)`
- Example could be `mb-2` which would mean a margin-bottom: 2.
- To activate dark-mode to your website, you just need to add `data-bs-theme="dark"` after your `<html lang="en">` but within the brackets obviously.
- Have a look at free bootstrap templates to get some ideas of templates.
- Have a look at the bootstrap template - saved in snippets on desktop.

### Web Design (CSS)

- You should always stick to two fonts for one design. These fonts should have similar moods and time era.
- You want to change the heading and body to be different type faces (i.e. serif vs sans-serif). As well as different weights.
- For text, should be 40-60 characters per line.
- Have a look at "F-layout" and "Z-layout" when designing your websites.

### Javascript (ES6) 

- ES is shorthand for ECMAScript (which is the european computer manufacturer's script).
- Java vs. Javascript - no relation whatsoever. Javascript is an interpreted programming language (meaning it kind of translates to the compiled language what to do - starts slowly and you can check how it is going during the process) whereas Java is a compiled programming language (meaning it does the job the interpreter has set out - starts quickly, but you can't really see what is happening throughout).
- Interpreted languages are languages such as Javascript, Python & Ruby - whereas compiled programming languages are like Java, C/C++, and Swift.
- When opening the JavaScript console, to write a double line of code, hold shift and press enter.
- Using the snippet editor of JavaScript console is a great way to write and test your code.
- `alert:("Hello");` - the `alert` is the FUNCTION (gets the browser to do something), `"Hello"` is the MESSAGE that you want displayed (AKA the STRING) and the `;` is the END of the instruction so that the browser doesn't get confused between one line and the other. 
- <strong>Data Types</strong> can include STRINGS (text we want to be displayed - it is a "string" of characters - these are immutable, meaning they cannot be changed), NUMBERS, & BOOLEAN (true/false).
- `typeof` - tells us what the data type is within the round brackets. I.e. `typeof(true)` would result in a BOOLEAN answer.
- <strong>Variables</strong> help to make the system "remember" the input.
- `var myName = "James";` - `var` is a KEY WORD (similar to alert and prompt) to tell us that we are creating a new data container. The `myName` is the NAME OF VARIABLE and the `"James"` is the STRING/VALUE.
- Variable names cannot start with numbers and cannot contain spaces or dashes. It is better to camelCase
- <strong>Strings</strong> can be combined using concantenation. `alert:("Hello" + " " + "Name");` would mean that it would equate to "Hello Name" on the pop up section.
- You can easily find out the number of characters in a string by stating word.length (variablename.length).
- The <strong>Slice(x,y)</string> function allows you to slice your strings to seperate them into individual characters. An example:
`var name = "James";`
`name.slice(0,1);` - would mean that the J is being selected. Programmers always start from 0, so although 'James' has 5 letters, S would be 4 (as J is 0). In order to grab the last letter though -
`name.slice(4,5);`
- `word.toUppercase()` - can turn every single character in a string to uppercase. Same with `word.toLower`
I am finding this super challenging...
- <strong>Numbers</strong> - you can add by `+`, subtract by `-`, division by `/`, multiply by `*`, but the <strong>modulo</strong> is represented by a `%` sign. The <strong>module</strong> will give you the remainder of the division (see below):
- `var a = 9 % 6; // 3` as this is the remainder of the 2 values.
- It is good programming practice to add a set of parantheses during BEDMAS protocols with numbers (even when you know this will happen by default).
- The <strong>Increment expression</strong> is another way of using `x = x+1` but you would use `x++` (which is the equivalent). `x = x-1` would be the same as `x--` and this would be the <strong>Decriment expression</strong>. You are only ever changing the value by one. If you need to increase by a specific number or variable, then you would use `x +=` and then by the number/variable, same with `x -=`. 
- 

