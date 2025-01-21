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
