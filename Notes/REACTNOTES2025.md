# REACT NOTES 2025

- React is a component based, state-driven javascript library for building UI - initially built by Facebook (most popular framework). 
- React is declarative (meaning we tell the component what it should look like based on current data/state - using JSX (HTML, CSS, JS and other).
- State or 'data' is the most important concept in React. Whenever we need something to change in the UI, we change the state. When the state changes, we manually update the state in our app, and then React will 'react' by re-rendering the UI for us.
- React is only the 'view' layer, if we want to build a real world application for routing/data fetching, we would use `Next.js`.
  
- JSX is declarative syntax to describe how components work and what they look like (based on their data and logic). It is an extension of JavaScript. 
- Next.js contains solutions for routing, data fetching and server side rendering.
 

- There are two options to create a React app - create-react-app (everything is already configured, comes with a development server and testing library - the problem with this however is that it is quite outdated - don't use these for BIG PROBLEMS - just tutorials/learning) or VITE (what you would want to use for your DearResident APP - need to manually set up ESlint, but is a lot faster).

- `Components` are the building blocks to create a complex application. They are basically functions that start with an uppercase letter. They also need to return some markup.
- We can call components multiple times in order to reuse it. 
- Each component has its own data, logic, and appearance.
- Make sure to wrap elements in a `<div></div>` element if you want to include more than one per component.

- `useState` is a React Hook that lets you add a state variable to your component.
- Pieces of data are called pieces of state. 
- `useEffect` is a React Hook that lets you synchronize a component with an external system. It takes 2 arguments - first a function, and the dependancy array.
- In React we try to divide user interfaces into components. All components should start with a capital letter i.e. below: 
`function Message() { return CODE }`

- <strong>Problems with using Vanilla JS</strong> -
  
<ol>
<li>It requires a lot of direct DOM manipulation and DOM traversing - this means that making bigger projects you would have a HUGE mess of code.</li>
  <li>Data/state is usually stored in the DOM, which can cause a lot of bugs.</li>
</ol>

- Front-end frameworks make it easier for us to keep UI and DATA in sync over time. React will update the UI automatically (so less work in code basically). They also give developers a consistent way of building front-end applications.

- <strong>Using Create-React-App</strong>
- To start: Go into the package.json file, have a look at scripts, and then start for the code.
- Open up the terminal. Then type 'npm start' - which will open up the new browser tab.
- To clear things on the terminal `ctrl c`. 
