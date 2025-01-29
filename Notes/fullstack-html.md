# Full-Stack Web Development Course Notes

## Table of Contents
1. [Frontend Development](#frontend-development)
    - [HTML](#html)
    - [CSS](#css)
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
