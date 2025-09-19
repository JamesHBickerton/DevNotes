# REACT NOTES 2025;

---

## What is React?
- **Component-based** & **state-driven** JavaScript library for building UIs.
- **Declarative**: The UI automatically reflects state/data changes.
- **View layer only** → Use **Next.js** for routing, data fetching, and server-side rendering.

---

## Why React vs Vanilla JS

| Vanilla JS | React |
|------------|-------|
| Manual DOM manipulation | Automatic UI updates |
| Data stored in DOM → prone to bugs | State-driven, clean data flow |
| Hard to scale | Components & hooks for maintainability |

---

## JSX
- JSX = JS + HTML + CSS syntax for UI
- **One root element per component** → use **Fragments (`<>...</>`)** for multiple elements
- Cannot use `if/else` or loops directly (use ternary operators or `map`)
- Use `className` instead of `class`

---
 
- There are two options to create a React app - create-react-app (everything is already configured, comes with a development server and testing library - the problem with this however is that it is quite outdated - don't use these for BIG PROBLEMS - just tutorials/learning) or VITE (what you would want to use for your DearResident APP - need to manually set up ESlint, but is a lot faster).

---

## Components
- `Components` are the building blocks to create a complex application. They are basically functions that start with an uppercase letter. They also need to return some markup. 
- We can call components multiple times in order to reuse it. Remember - data can only flow one way - from parent to child. This is different from Angular. 
- Each component has its own data (props and state), logic, and appearance.
- Make sure to wrap elements in a `<div></div>` element if you want to include more than one per component.
- `React.createElement(type, props, ...children)`
- The `type` must be a valid React component type. The `prop` must be an object or 'null'. The `...children` is optional, and can be any React nodes or elements.
- In JSX we do not use `class='container'` we would use `className='container'`.

---

## Props
- `Props` are how we pass data from parent to child components. <strong>They are immutable!!</strong>.
- If you need to mutate props, then you need `state`. 
- In the parent component you would define what you want i.e. `name="Pizza Spinaci"`.
- Then to pass it onto the child you would pass a `props` parameter into the child component. and then enter for example - `<h3>{props.name}</h3>`.
- Props data can only be updated by the parent component (as it is the parent's component that 'owns' the data).
- To avoid having to use the `.props` in all of your components, you can destructure the object you want to use in your parameter for the component. 

- Pieces of data are called pieces of state. 
- `useEffect` is a React Hook that lets you synchronize a component with an external system. It takes 2 arguments - first a function, and the dependancy array.
- In React we try to divide user interfaces into components. All components should start with a capital letter i.e. below: 
`function Message() { return CODE }`

- <strong>Using Create-React-App</strong>
- To start: Go into the package.json file, have a look at scripts, and then start for the code.
- Open up the terminal. Then type 'npm start' - which will open up the new browser tab.
- To clear things on the terminal `ctrl c`.

---

## Rendering Lists
- To create multiple components from an array of data you would render a list (usually using the .map() method).
- `array.map((item, index) => <Component key={uniqueKey} prop={item.prop} />)`
- Components can also be 'conditionally rendered' based on a condition (i.e. using the ternary operator). 

---

## React Fragments
- <strong>React Fragments</strong> - lets us group together elements without leaving any trace in the DOM tree (if you want to have more than one element in a component).
- Fragments are empty `<>` that allow us to add more than one element, without messing with the formatting. This won't create any new element.
- Sometimes you need to add keys to react fragments (i.e. when rendering lists). To do this: `<React.fragment>code</React.fragment>`

---

- You can use the `onClick` prop to use an inline feature for your JSX. The 'Click' is the event name, and the prefix is the 'on'. Example:
- `onClick={function}`  - just important to note we are handing in the function value, not calling the function. 
- Similar to the `onMouseEnter` prop is used when the mouse 'enters' the element - i.e. moves across it. 

---

## State
- State is the most important concept in React. State is data that a component can hold over time (think of it as the memory for a certain component).
- A `piece of state` or `state variable` is just ONE variable in a component that we can define in our code.
- Updating a piece of state triggers React to re-render a component in the UI - to create a new updated view.

- To add a new piece of state, we use 3 steps:
<ol>
 <li>We add a new state variable</li>
 <li>We use it in the code - usually JSX</li>
 <li>We then update the piece of state in some event handler</li>
</ol>

- `useState` is a `hook` lets you add a state variable to your component. It will return an array. The first value is the default value we want for the state, and the second value is the function we can use to update your state variable - so usually we destructure the array first i.e. `const [step, setStep] = useState(1);`.
- We can only call hooks on the top level of the function (i.e. not inside a function or loop/if statement etc).
- For data that should not trigger a re-render, you don't have to use state for this (common for beginners to use state for everything). Just use a variable instead. 

---

## Forms

- When using form it's good practice (when using a function in JS) to e.preventDefault() - just to prevent the page from reloading.

---

## Controlled Elements

- This is a way to keep data inside of the application (state) and not the DOM.
- First, create a piece of state. I.e. `const [description, setDescription] = useState("")`.
- Use state to choose the input field you want to control - i.e. if it was an input: `<input type="text' placeholder="item..." value={description} onChange={(e) => setDescription(e.target.value)}/>`
  
