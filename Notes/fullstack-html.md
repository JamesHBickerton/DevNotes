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


