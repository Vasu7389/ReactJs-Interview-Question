---
title: "React Js Interview Questions & Answers 2026 - Modern React, TypeScript & Best Practices"
description: "Master React interviews! Comprehensive guide with 90+ questions covering React 19, Server Components, TypeScript, testing, performance, security, and advanced patterns."
githubPath: "https://github.com/PankajSingh34/ReactJs-Interview-Question"
---

<span style=" font-size: 1rem; border-bottom: 1px solid grey;"> Updated January 12, 2026 </span>

Here you'll find **90+ comprehensive React.js interview questions and answers** covering everything from fundamentals to advanced patterns. Perfect for freshers, experienced developers, and everyone in between preparing for React interviews at top companies.

## What's New in 2026 Edition?

✨ **React 19 Features** - Latest hooks, Server Components, and React Compiler  
🔷 **TypeScript Integration** - Advanced patterns and type-safe React development  
🧪 **Modern Testing** - React Testing Library, Jest, and accessibility testing  
🚀 **Performance** - Advanced optimization techniques and best practices  
🔒 **Security & A11y** - Security vulnerabilities and accessibility implementation  
📐 **Advanced Patterns** - Compound components, render props, and modern architecture

## What's New in 2026 Edition?

✨ **React 19 Features** - Latest hooks, Server Components, and React Compiler  
🔷 **TypeScript Integration** - Advanced patterns and type-safe React development  
🧪 **Modern Testing** - React Testing Library, Jest, and accessibility testing  
🚀 **Performance** - Advanced optimization techniques and best practices  
🔒 **Security & A11y** - Security vulnerabilities and accessibility implementation  
📐 **Advanced Patterns** - Compound components, render props, and modern architecture

## 📚 Table of Contents

1. **[React Fundamentals](#react-js-interview-questions)** (Questions 1-52)

   - Basic concepts, components, hooks, lifecycle methods
   - State management, props, JSX, Virtual DOM

2. **[React 19 & Modern Features](#react-19-features--modern-react)** (Questions 79-83)

   - New `use()` hook, React Compiler, Server Components
   - App Router, Suspense, and concurrent features

3. **[Performance & TypeScript](#performance-optimization--typescript)** (Questions 84-85)

   - Advanced memoization, useMemo, useCallback
   - TypeScript patterns, generic components, type safety

4. **[Testing & Quality](#react-testing--best-practices)** (Question 86)

   - React Testing Library, custom hook testing
   - Component testing, mocking, accessibility testing

5. **[Security & Accessibility](#react-security--accessibility)** (Questions 87-88)

   - XSS prevention, authentication, CSRF protection
   - Screen readers, ARIA, keyboard navigation

6. **[Advanced Patterns](#advanced-react-patterns)** (Questions 89-90)

   - Compound components, render props
   - Custom hooks vs render props comparison

7. **[Coding Challenges](#react-js-coding-test-questions-and-qnswers)** (Questions 53-78)
   - Practical implementations, scenario-based problems
   - Real-world examples and best practices

## ReactJs

ReactJs is a popular JavaScript library for building user interfaces. It is maintained by Facebook, and is widely used for building web applications, mobile apps, and other user interfaces. React allows developers to create reusable components, which can help make large applications easier to manage and maintain. It is designed to be efficient, declarative, and flexible, and can be used to create complex, dynamic user interfaces.

Looking to expand your knowledge on Javascript as well? Check out our comprehensive collection of <span style="text-decoration: underline;color: var(--theme-primary-color);">
[JavaScript interview question and answers page](https://www.codinn.dev/tricky-javascript/es6789-code-snippets-interview-questions)
</span> to help you prepare for your next interview.

<span style=" font-size: 1rem;">\*Discover the answers by clicking on the questions.</span>

> **💡 Important Note for 2026:** This guide has been extensively updated with modern React practices. While legacy patterns (like deprecated lifecycle methods) are mentioned for completeness, we strongly recommend using the modern equivalents (hooks, TypeScript, etc.) shown throughout this guide.

## React Js Interview Questions

<details>
<summary>
    <h3>1. How does React work?</h3>
</summary>

React creates a virtual DOM. When the state changes in a component it first runs a "diffing" algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff.

</details>

<details>
<summary>
    <h3>2. What are the advantages of using React?</h3>
</summary>

- It is easy to know how a component is rendered, you just need to look at the render function.
- JSX makes it easy to read the code of your components. It is also really easy to see the layout, or how components are plugged/combined.
- You can render React on the server side. This improves SEO and performance.
- It is easy to test.
- You can use React with any framework you wish as it is only a view layer.

</details>

<details>
<summary>
    <h3>3. What is the difference between a Presentational component and a Container component?</h3>
</summary>

Presentational components are concerned with how things look. They generally receive data and callbacks exclusively via props. These components rarely have their own state, but when they do it generally concerns UI state, as opposed to data state.

When your component just receives props and renders them to the page, this is a `stateless component`, for which a pure function can be used. These are also called dumb components or presentational components.

Container components are more concerned with how things work. These components provide the data and behavior to presentational or other container components. They define actions and provide these as callbacks to the presentational components. They are also often stateful as they serve as data sources.

</details>

<details>
<summary>
    <h3>4. What are the differences between a class component and functional component?</h3>
</summary>

- The class component uses ES6 class syntax, and it extends React components with a render method that returns React elements.

- Functional components with hooks are purely JavaScript functions that also return React elements. Before the introduction of hooks, functional components were stateless.

</details>

<details>
<summary>
    <h3>5. What is the difference between state and props?</h3>
</summary>

State is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.

Props (short for properties) are a Component's configuration. They are received from above and immutable as far as the Component receiving them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Components. Callback functions can also be passed in as props.

</details>

<details>
<summary>
    <h3>6. What are the different lifecycle methods?</h3>
</summary>

- `componentWillMount` (deprecated) - this is most commonly used for App configuration in your root component.
- `componentDidMount` - here you want to do all the setup you couldn’t do without a DOM, and start getting all the data you need. Also if you want to set up eventListeners etc. this lifecycle hook is a good place to do that.
- `componentWillReceiveProps` (deprecated) - this lifecyclye acts on particular prop changes to trigger state transitions.
- `shouldComponentUpdate` - if you’re worried about wasted renders shouldComponentUpdate is a great place to improve performance as it allows you to prevent a rerender if component receives new prop. shouldComponentUpdate should always return a boolean and based on what this is will determine if the component is rerendered or not.
- `componentWillUpdate` (deprecated) - rarely used. It can be used instead of componentWillReceiveProps on a component that also has shouldComponentUpdate (but no access to previous props).
- `componentDidUpdate` - also commonly used to update the DOM in response to prop or state changes.
- `componentWillUnmount` - enables you can cancel any outgoing network requests, or remove all event listeners associated with the component.

</details>

<details>
<summary>
    <h3>7. Explain React Hooks.</h3>
</summary>

Hooks let you use more of React’s features without having to use classes. The first hook that you will most likely encounter is useState. useState is a Hook that lets you add React state to function components. It returns an array with a getter and a setter.

The syntax looks like

```jsx
const [count, setCount] = React.useState(0);

<button onClick={() => setCount(count + 1)}>Increase Count</button>;
```

The equivalent when using a class component would be.

```jsx
this.state = {
  count: 0,
};

<button onClick={() => this.setState({ count: this.state.count + 1 })}>
  Increase Count
</button>;
```

The next hook you will most likely encounter is useEffect. The Effect Hook lets you perform side effects in function components. By passing an empty array as the second argument to useEffect is equivalent to using componentDidMount. If you pass a value to the array it will only call the useEffect function when the value in the array updates.

```jsx
useEffect(() => {
  // do stuff when the component mounts
}, []);
```

</details>

<details>
<summary>
    <h3>8. Where in a React class component should you make an AJAX/API request?</h3>
</summary>

`componentDidMount` is where an AJAX request should be made in a React component. This method will be executed when the component `mounts` (is added to the DOM) for the first time. This method is only executed once during the component’s life. Importantly, you can’t guarantee the AJAX request will have resolved before the component mounts. If it doesn't, that would mean that you’d be trying to setState on an unmounted component, which would not work. Making your AJAX request in `componentDidMount` will guarantee that there is a component to update.

</details>

<details>
<summary>
    <h3>9. What are controlled components?</h3>
</summary>

In HTML, form elements such as `<input>`, `<textarea>`, and `<select>` typically maintain their own state and update it based on user input. When a user submits a form the values from the mentioned elements are sent with the form. With React it works differently. The component containing the form will keep track of the value of the input in it's state and will re-render the component each time the callback function e.g. onChange is fired as the state will be updated. An input form element whose value is controlled by React in this way is called a `controlled component`.

</details>

<details>
<summary>
    <h3>10. What are refs used for in React?</h3>
</summary>

Refs are used to get reference to a DOM node or an instance of a component in React. Good examples of when to use refs are for managing focus/text selection, triggering imperative animations, or integrating with third-party DOM libraries. You should avoid using string refs and inline ref callbacks. Callback refs are advised by React.

</details>

<details>
<summary>
    <h3>11. What is a higher order component?</h3>
</summary>

A higher-order component is a function that takes a component and returns a new component. HOC's allow you to reuse code, logic and bootstrap abstraction. The most common is probably Redux’s connect function. Beyond simply sharing utility libraries and simple composition, HOCs are the best way to share behavior between React Components. If you find yourself writing a lot of code in different places that does the same thing, you may be able to refactor that code into a reusable HOC.

</details>

<details>
<summary>
    <h3>12. What advantages are there in using arrow functions?</h3>
</summary>

- Scope safety: Until arrow functions, every new function defined its own this value (a new object in the case of a constructor, undefined in strict mode function calls, the base object if the function is called as an "object method", etc.). An arrow function does not create its own this, the this value of the enclosing execution context is used.
- Compactness: Arrow functions are easier to read and write.
- Clarity: When almost everything is an arrow function, any regular function immediately sticks out for defining the scope. A developer can always look up the next-higher function statement to see what the Object is.
</details>

<details>
<summary>
    <h3>13. How would you prevent a class component from rendering?</h3>
</summary>

Returning null from a component's render method means nothing will be displayed, but it does not affect the firing of the component's lifecycle methods.

If the amount of times the component re-renders is an issue, there are two options available. Manually implementing a check in the `shouldComponentUpdate` lifecycle method hook.

```jsx
shouldComponentUpdate(nextProps, nextState){
  const allowRender = true;
  // Do some check here and assign decicison to allowRender
  return allowRender
}
```

Or using React.PureComponent instead of React.Component React.PureComponent implements shouldComponentUpdate() with a shallow prop and state comparison. This enables you to avoid re-rendering the component with the same props and state.

</details>

<details>
<summary>
    <h3>14. When rendering a list what is a key and what is it's purpose?</h3>
</summary>

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys. When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort. It is not recommend to use indexes for keys if the items can reorder, as that would be slow.

</details>

<details>
<summary>
    <h3>15. What is the purpose of `super(props)` ?</h3>
</summary>

A child class constructor cannot make use of this until `super()` has been called. Also, ES2015 class constructors have to call `super()` if they are subclasses. The reason for passing props to `super()` is to enable you to access `this.props` in the constructor.

</details>

<details>
<summary>
    <h3>16. What is JSX?</h3>
</summary>

- JSX is a syntax extension to JavaScript and comes with the full power of JavaScript. JSX produces React `elements`.
- You can embed any JavaScript expression in JSX by wrapping it in curly braces. After compilation, JSX expressions become regular JavaScript objects.
- This means that you can use JSX inside of `if` statements and `for loops`, assign it to variables, accept it as arguments, and return it from functions.

</details>

<details>
<summary>
    <h3>17. What is equivalent of the following using React.createElement?</h3>
</summary>

```jsx
const element = <h1 className="greeting">Hello, world!</h1>;
```

```jsx
const element = React.createElement(
  "h1",
  { className: "greeting" },
  "Hello, world!"
);
```

</details>

<details>
<summary>
    <h3>18. What is redux?</h3>
</summary>

- The basic idea of redux is that the entire application state is kept in a single store. The store is simply a javascript object.
- The only way to change the state is by sending actions from your application and then writing reducers for these actions that modify the state.
- The entire state transition is kept inside reducers and should not have any `side-effects`.

</details>

<details>
<summary>
    <h3>19. What is a store in redux?</h3>
</summary>

The store is a javascript object that holds application state. Along with this it also has the following responsibilities:

- Allows access to state via `getState();`.
- Allows state to be updated via `dispatch(action);`.
- Registers listeners via `subscribe(listener);`.
- Handles unregistering of listeners via the function returned by `subscribe(listener)`.

</details>

<details>
<summary>
    <h3>20. Difference between action and reducer.</h3>
</summary>

- Actions are plain javascript objects.
- They must have a type indicating the type of action being performed.
- In essence, actions are payloads of information that send data from your application to your store.

A reducer is simply a pure function that takes the previous state and an action, and returns the next state.

</details>

<details>
<summary>
    <h3>21. What is Redux Thunk used for?</h3>
</summary>

- Redux thunk is middleware that allows you to write action creators that return a function instead of an action.
- The thunk can then be used to delay the dispatch of an action if a certain condition is met. This allows you to handle the asynchronous dispatching of actions.

</details>

<details>
<summary>
    <h3>22. Write a custom hook which can be used to debounce user's input.</h3>
</summary>

```jsx
//hook
const useDebounce = (value, delay) => {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timeout = setTimeout(() => {
      setDebouncedValue(value);
    }, delay);

    return () => {
      clearTimeout(timeout);
    };
  }, [value]);

  return debouncedValue;
};

//example
const Counter = () => {
  const [value, setValue] = useState(0);
  const lastValue = useDebounce(value, 1000);

  return (
    <div>
      <p>
        Current Value: {value} | Debounced Value: {lastValue}
      </p>
      <button onClick={() => setValue(value + 1)}>Increment</button>
    </div>
  );
};
```

</details>

<details>
<summary>
    <h3>23. Write a custom hook to copy text to clipboard.</h3>
</summary>

```jsx
// hook
function useCopyToClipboard(content) {
  const [isCopied, setIsCopied] = useState(false);

  const copy = useCallback(() => {
    navigator.clipboard
      .writeText(content)
      .then(() => setIsCopied(true))
      .then(() => setTimeout(() => setIsCopied(false), 1250))
      .catch((err) => alert(err));
  }, [content]);
  return [isCopied, copy];
}

// usage
export default function App() {
  const [isCopied, copy] = useCopyToClipboard("Text to copy!");
  return <button onClick={copy}>{isCopied ? "Copied!" : "Copy"}</button>;
}
```

</details>

<details>
<summary>
    <h3>24. How to Use the 'useId' Hook to generate unique ids.</h3>
</summary>

- useId does not take any parameters.

- useId returns a unique ID string associated with this particular useId call in this particular component.

```jsx
//usage
import { useId } from "react";

const App = () => {
  const id = useId();

  return (
    <form>
      <label htmlFor={`email-${id}`}>Email</label>
      <input type="text" id={`email-${id}`} name="email" />

      <label htmlFor={`password-${id}`}>Password</label>
      <input type="password" id={`password-${id}`} name="password" />
    </form>
  );
};

// 🔴 Bad Practise - Don't use for key
const id = useId();

return posts.map((post) => <article key={id}>...</article>);
```

</details>

<details>
<summary>
    <h3>25. How to validate Props in React?</h3>
</summary>

- We can use 'prop-types' package

- Earlier, till React v15.5 this was there as part of React iteslf

```jsx
import PropTypes from "prop-types";

function MyComponent({ name }) {
  return <div>Hello, {name}</div>;
}

MyComponent.propTypes = {
  name: PropTypes.string,
};

export default MyComponent;
```

</details>

<details>
<summary>
    <h3>26. Give a practical example of Higher Order Component in react.</h3>
</summary>

- Show a loader while a component waits for data

```jsx
//HOC
function WithLoading(Component) {
  return function WihLoadingComponent({ isLoading, ...props }) {
    if (!isLoading) return <Component {...props} />;
    return <p>Please wait, fetching your data in no time...</p>;
  };
}
export default WithLoading;

//usage
import UserListComponent from "./UserListComponent.js"; //importing component
import WithLoading from "./withLoading.js"; //importing HOC
const ListWithLoading = WithLoading(UserListComponent); //connect component with HOC

const App = () => {
  const [loading, setLoading] = useState(true);
  const [users, setUsers] = useState([]);
  useEffect(() => {
    //fetch data
    const dataFromApi = ["this is coming from API call", "don't show loader"];
    //at this time loader will be shown in the UI using HOC
    //data fetched successfully
    setUsers([...dataFromApi]);
    setLoading(false);
  }, []);

  return <ListWithLoading isLoading={loading} users={users} />;
};
```

</details>

<details>
<summary>
    <h3>27. Why React's useDeferredValue hook is useful?</h3>
</summary>

- 'useDeferredValue' is a React Hook that lets you defer updating a part of the UI.

- Basically it let you perform the debouncing technique with lesser code.

```jsx
//usage
import { useState, useDeferredValue } from "react";
//userList component takes searchText to fetch user's list
import UserList from "./UserList.js";

export default function App() {
  const [searchText, setSearchText] = useState("");
  //pass searchText as default visible value in useDeferredValue
  const deferredQuery = useDeferredValue(searchText);

  return (
    <>
      <label>
        Search user:
        <input
          value={searchText}
          onChange={(e) => setSearchText(e.target.value)}
        />
      </label>
      <div>
        <UserList searchText={deferredQuery} />
      </div>
    </>
  );
}
```

</details>

<details>
<summary>
    <h3>29. How to detect 'click' outside React component?</h3>
</summary>

```jsx
export default function OutsideAlerter() {
  const clickMeDivRef = useRef(null);

  useEffect(() => {
    const handleClickOutside = (event) => {
      if (!ref?.current?.contains(event.target)) {
        alert("You clicked outside of me!");
      }
    };

    // Bind the event listener
    document.addEventListener("mousedown", handleClickOutside);

    return () => {
      // Unbind the event listener on clean up
      document.removeEventListener("mousedown", handleClickOutside);
    };
  }, [clickMeDivRef]);

  return <div ref={clickMeDivRef}>Clicked me?</div>;
}
```

</details>

<details>
<summary>
    <h3>30. Why do React component names have to start with capital letters?</h3>
</summary>

In JSX, lowercase tag names are considered to be HTML tags. However, lowercase tag names with a dot (property accessor) aren't.

- `<person />` compiles to React.createElement('person') (html tag)
- `<Person />` compiles to React.createElement(Person)
- `<obj.person />` compiles to React.createElement(obj.person)

```jsx
// Wrong! This is a component and should be in uppercase.
function person(props) {
  // Correct! This usage of <div> is correct because div is a valid element.
  return <div>{props.isLearning ? "Great!" : "Call Mom!"}</div>;
}

function App() {
  // Wrong! React thinks <person /> is a HTML tag because it's not capitalized.
  return <person isLearning={true} />;
}

// Correct! This is a component and should be capitalized
function Person(props) {
  // Correct! This usage of <div> is correct because div is a valid element.
  return <div>{props.isLearning ? "Great!" : "Call Mom!"}</div>;
}

function App() {
  // Correct! React knows <Person /> is a component because it's capitalized.
  return <Person isLearning={true} />;
}
```

</details>

<details>
<summary>
    <h3>31. What is the difference between npx and npm?</h3>
</summary>

- NPM is a package manager and can be used to install node.js packages.
- NPX is a tool to execute node.js packages.

It doesn't matter whether you installed that package globally or locally. NPX will temporarily install it and run it. NPM also can run packages if you configure a package.json file.

So if you want to check/run a node package quickly without installing it - use NPX.

'create-react-app' is a npm package that is expected to be run only once in a project's lifecycle. Hence, it is preferred to use npx to install and run it in a single step.

```bash
> npx create-react-app codinn
```

```bash
npM - Manager
```

```bash
npX - Execute
```

</details>

<details>
<summary>
    <h3>32. How to set focus on an input field after component mounts on UI?</h3>
</summary>

```jsx
import React, { useEffect, useRef } from "react";

const SearchPage = () => {
  const textInput = useRef(null);

  useEffect(() => {
    textInput.current.focus();
  }, []);

  return (
    <div>
      <input ref={textInput} type="text" />
    </div>
  );
};
```

</details>

<details>
<summary>
    <h3>33. How to programmatically navigate using latest React Router version?</h3>
</summary>

```jsx
//old - v5
import { useHistory } from "react-router-dom";

function HomeButton() {
  let history = useHistory();
  history.push('/some/path') here
};

//new - v6+
import { useNavigate } from "react-router-dom";

function SignupForm() {
  let navigate = useNavigate();

  async function handleSubmit(event) {
    event.preventDefault();
    await submitForm(event.target);
    navigate("../success", { replace: true });
  }

  return <form onSubmit={handleSubmit}>{/* ... */}</form>;
}

//or
import { redirect } from "react-router-dom";

const loader = async () => {
  const user = await getUser();
  if (!user) {
    return redirect("/login");
  }
};
```

</details>

<details>
<summary>
    <h3>34. What is React state batching? Guess the output.</h3>
</summary>

Given Snippet

```jsx
export default function Counter() {
  const [number, setNumber] = useState(0);

  return (
    <>
      <h1>{number}</h1>
      <button
        onClick={() => {
          setNumber(number + 1);
          setNumber(number + 1);
          setNumber(number + 1);
        }}
      >
        +3
      </button>
    </>
  );
}
```

Output

- on click of '+3' -> prints '1'
- or update state only once because of state batching concept

Why?

This lets you update multiple state variables without triggering too many re-renders.

But if you want to update anyways? That is - it need to print 3 on click of '+3'.

Pass the callback method to `setNumber`.

```js
setNumber((n) => n + 1);
```

```jsx
return (
  <>
    <h1>{number}</h1>
    <button
      onClick={() => {
        setNumber((n) => n + 1);
        setNumber((n) => n + 1);
        setNumber((n) => n + 1);
      }}
    >
      +3
    </button>
  </>
);
```

</details>

<details>
<summary>
    <h3>35. How to pass data between sibling components using React router?</h3>
</summary>

Passing data between sibling components of React is possible using React Router `useParams` hook.

Parent component (usually App.js to define routes)

```jsx
<Route path="/user/:id" element={<User />} />
```

```jsx
import { useParams } from "react-router-dom";

const User = () => {
  let { id } = useParams();

  useEffect(() => {
    console.log(`/user/${id}`);
  }, []);

  // .....
};
```

</details>

<details>
<summary>
    <h3>36. How to access a global variable using useContext hook?</h3>
</summary>

```jsx
//1. create context
const GlobalLanguageContext = React.createContext(null);

const App = () => {
  const contextValue = { language: "EN" };

  return (
    //2. connect with all the child components under Provider
    //One time Config - Here in Provider's value prop you can pass
    //the value of your context global variable
    <GlobalLanguageContext.Provider value={contextValue}>
      <Child />
    </GlobalLanguageContext.Provider>
  );
};

const Child = () => {
  //3. use variable
  const { language } = React.useContext(GlobalLanguageContext);
  return <div>Application Language: {language}</div>;
};
```

</details>

<details>
<summary>
    <h3>37.  What is the difference between useMemo and useCallback?</h3>
</summary>

- useCallback gives you referential equality between renders for functions. And useMemo gives you referential equality between renders for values.
- useCallback and useMemo both expect a function and an array of dependencies. The difference is that useCallback returns its function when the dependencies change while useMemo calls its function and returns the result.
- useCallback returns its function uncalled so you can call it later, while useMemo calls its function and returns the result

</details>

 <details>
<summary>
    <h3>38. Why you should prefer vite over create-react-app?</h3>
</summary>

- Create React App (CRA) has long been the go-to tool for most developers to scaffold React projects and set up a dev server. It offers a modern build setup with no configuration.
- But, we see increased development and build time when the project size increases. This slow feedback loop affects developer's productivity and happiness.
- To address these issues, there is a new front-end tooling in the ecosystem: `Vite`.
- Unlike CRA, Vite does not build your entire application before serving, instead, it builds the application on demand. It also leverages the power of native ES modules, esbuild, and Rollup to improve development and build time.
- Vite is a next-generation, front-end tool that focuses on speed and performance.
- Vite is a development server that provides rich feature enhancements over native ES modules: fast Hot Module Replacement (HMR), pre-bundling, support for typescript, jsx, and dynamic import.
- A build command that bundles your code with Rollup, pre-configured to output optimized static assets for production.

</details>

<details>
<summary>
    <h3>39. What are the advantages of react-router?</h3>
</summary>

- The major advantage of `react-router` is that the page does not have to be refreshed when a link to another page is clicked.
- It also allows us to use browser's `history` feature while preserving the right application view.
- Better user experience, animations and transitions can be easily implemented when switching between different components.
- React Router uses `dynamic routing` to ensure that routing is achieved as it is requested by the user. This also means that all the required components are also rendered without any flashes of white screen or page reload.
- The main components of `react-router` are: `BrowserRouter`, `Routes`, `Route`, `Link`.

</details>

<details>
<summary>
    <h3>40. How can you optimize performance in a ReactJS application?</h3>
</summary>

- One way is to use the shouldComponentUpdate lifecycle method to prevent unnecessary re-renders of a component.
- Another way is to use the PureComponent class, which implements shouldComponentUpdate with a shallow comparison of props and state.
- Additionally, using the React.memo higher-order component can optimize the performance of functional components.

</details>

<details>
<summary>
    <h3>41. Write code for CRUD functionality in ReactJs?</h3>
</summary>

To implement CRUD (create, read, update, delete) functionality in a React application using hooks, you can use the useState hook to manage the state of your application and the useEffect hook to handle side effects, such as making API calls to a server to create, read, update, or delete data.

Here is an example of how you might implement CRUD functionality in a React component using hooks:

```jsx
import React, { useState, useEffect } from "react";

function App() {
  // useState hook to manage the state of our items
  const [items, setItems] = useState([]);

  // useEffect hook to fetch the items from an API
  useEffect(() => {
    fetch("https://my-api.com/items")
      .then((response) => response.json())
      .then((data) => setItems(data));
  }, []);

  // helper function to add a new item
  const addItem = (name) => {
    const newItem = { name };
    setItems([...items, newItem]);
  };

  // helper function to update an item
  const updateItem = (index, name) => {
    const updatedItems = [...items];
    updatedItems[index] = { name };
    setItems(updatedItems);
  };

  // helper function to delete an item
  const deleteItem = (index) => {
    const updatedItems = [...items];
    updatedItems.splice(index, 1);
    setItems(updatedItems);
  };

  // render the items in a list
  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>
          {item.name}
          <button onClick={() => updateItem(index, "updated name")}>
            Update
          </button>
          <button onClick={() => deleteItem(index)}>Delete</button>
        </li>
      ))}
      <button onClick={() => addItem("new item")}>Add item</button>
    </ul>
  );
}
```

</details>

<details>
<summary>
 <h3>42. What is a hook in React and why are they useful? </h3>
</summary>

A hook in React is a function that allows developers to use state and other React features without writing a class. This makes it possible to use these features in functional components, which can be easier to write and understand than class-based components.

</details>

<details>
<summary>
 <h3>43. What are some common hooks that are used in React? </h3>
</summary>

Some common hooks that are used in React include useState, useEffect, and useContext. The useState hook allows a functional component to have local state, the useEffect hook allows a functional component to perform side effects, and the useContext hook allows a functional component to access values from the nearest context provider.

</details>

<details>
<summary>
 <h3>44. Can you use hooks inside a class-based component? </h3>
</summary>

No, hooks can only be used inside functional components. If you need to use state or other React features in a class-based component, you will need to use a class component.

</details>

<details>
<summary>
    <h3>45. How do you test a component that uses hooks? </h3>
</summary>

You can test a component that uses hooks by using the act utility from the react-testing-library package. This utility allows you to simulate the effects of React's reconciliation process, which is necessary for hooks to work correctly. You can then use standard Jest or Enzyme assertions to verify the behavior of your component.

</details>

<details>
<summary>
    <h3>46. What is the useEffect hook used for? </h3>
</summary>

The useEffect hook is used for performing side effects in functional components. This can include things like data fetching, setting up subscriptions, or manually changing the DOM. The useEffect hook is called after the component renders, and can be used to ensure that your component stays up-to-date with any relevant data or dependencies.

</details>

<details>
<summary>
    <h3>47. Create a simple custom hook in React? </h3>
</summary>

To create a custom hook in React, you can use the useState hook to add local state to a functional component. Here's an example:

```jsx
import { useState } from "react";

function useCounter() {
  const [count, setCount] = useState(0);

  function increment() {
    setCount(count + 1);
  }

  return { count, increment };
}
```

This hook adds a count state and an increment function to a component. To use this hook in a component, you can call it at the top of the component function, like this:

```jsx
function MyComponent() {
  const { count, increment } = useCounter();

  return (
    <div>
      <p>The count is {count}.</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```

Now, whenever the increment button is clicked, the count state will be updated and the component will re-render with the new value.

</details>

<details>
<summary>
    <h3>48. What is the difference between useEffect and useLayoutEffect? </h3>
</summary>

Here is an example of how you might use useEffect and useLayoutEffect in a React component:

```jsx
import React, { useState, useEffect, useLayoutEffect } from "react";

function MyComponent() {
  const [count, setCount] = useState(0);

  // useEffect runs after the render cycle has completed
  useEffect(() => {
    // This code will run every time the component renders,
    // after the render is complete.
    console.log("useEffect running");
  });

  // useLayoutEffect runs synchronously immediately after the render cycle
  useLayoutEffect(() => {
    // This code will run every time the component renders,
    // before the browser has a chance to paint the update to the screen.
    // Be careful! This can cause visual inconsistencies.
    console.log("useLayoutEffect running");
  });

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

In this example, when the Increment button is clicked, the useEffect hook will run after the component has been updated and re-rendered, whereas the useLayoutEffect hook will run before the update is painted to the screen. This means that if you were to use useLayoutEffect to update the UI, the user might see the UI update before the update is complete, which can cause visual inconsistencies. useEffect, on the other hand, runs after the update is complete and is therefore safer to use for updating the UI.

</details>

<details>
<summary>
    <h3>49. Why virtual DOM is faster to update than real DOM? </h3>
</summary>

- The virtual DOM is faster to update than the real DOM because React uses a clever technique to minimize the number of updates that need to be made to the real DOM.

- When you update the virtual DOM, React will compare the new virtual DOM with the old one, determine which parts have changed, and then update the real DOM accordingly. This means that only the parts of the DOM that actually need to be changed are updated, which is much faster than updating the entire DOM every time there is a change.

- Furthermore, the virtual DOM is implemented in JavaScript, which is generally faster to execute than the native code that is used to manipulate the real DOM.

- This means that React can perform updates to the virtual DOM quickly, and then use the resulting diff to make efficient updates to the real DOM.

Overall, the use of the virtual DOM allows React to make efficient updates to the UI, which results in a faster and more responsive user experience.

</details>

<details>
<summary>
    <h3>50. Can you explain the difference between a pure and impure function, and why it matters in the context of React? </h3>
</summary>

In React, a pure function is a function that returns the same output for the same set of inputs, regardless of when it is called. An impure function, on the other hand, is a function that may produce different outputs for the same set of inputs, depending on when it is called or other factors.

Here is an example of a pure function in React:

```jsx
function addNumbers(a, b) {
  return a + b;
}
```

This function takes in two numbers, a and b, and returns their sum. This function will always return the same result for the same input, regardless of when it is called or what state the component is in.

Here is an example of an impure function in React:

```jsx
function getRandomNumber() {
  return Math.random();
}
```

This function returns a random number every time it is called. Because the output of this function depends on factors outside of its control (in this case, the current time and a random seed), it is considered an impure function.

In general, pure functions are preferred in React because they are easier to reason about and test. Impure functions, on the other hand, can introduce unpredictable behavior and make your code more difficult to understand.

</details>

<details>
<summary>
    <h3>51. Explain Styled Component in React with example? </h3>
</summary>

Styled Components is a library for React and React Native that allows you to write actual CSS code to style your components. It allows you to write your styles in a declarative way alongside your components, rather than having to maintain separate style sheets.

Here is an example of using Styled Components in a React component:

```jsx
import styled from "styled-components";

const Button = styled.button`
  background: palevioletred;
  border-radius: 3px;
  border: none;
  color: white;
`;

function MyComponent() {
  return <Button>Click me!</Button>;
}
```

In this example, the Button component is styled with a pale violet red background and white text. The styles are written within a template literal and are applied to the button element. When the Button component is rendered, it will have these styles applied to it.

Styled Components allows you to easily customize your styles based on props passed to the component. For example:

```jsx
const Button = styled.button`
  background: ${(props) => (props.primary ? "palevioletred" : "white")};
  border-radius: 3px;
  border: none;
  color: ${(props) => (props.primary ? "white" : "palevioletred")};
`;

function MyComponent() {
  return (
    <div>
      <Button>Click me!</Button>
      <Button primary>Click me!</Button>
    </div>
  );
}
```

In this example, the Button component has a customizable background and text color based on the primary prop. The first Button will have a white background and pale violet red text, while the second Button will have a pale violet red background and white text.

</details>

<details>
<summary>
    <h3>52. Styled-Components vs Inline Styling in React? </h3>
</summary>

It really depends on your specific needs and preferences. Both inline styling and Styled Components have their own advantages and disadvantages, and the best choice for you will depend on the requirements of your project.

Inline styling refers to the practice of applying styles directly to elements using the style attribute. In React, this can be done using the style prop on elements. For example:

```jsx
function MyComponent() {
  return <div style={{ color: "red", fontSize: "20px" }}>Hello, World!</div>;
}
```

One advantage of inline styling is that it can be very simple to use and understand. There's no need to import additional libraries or set up complex configurations. Inline styling also allows you to easily apply styles based on props or state, which can be very useful in certain situations.

However, inline styling can also have some drawbacks. It can make your code more cluttered and harder to read, especially for complex styles. It can also be more difficult to reuse styles across different components, as you would need to copy and paste the style objects between components.

Styled Components is a library that allows you to define styles using actual CSS syntax and apply them to React components. It allows you to write your styles in a declarative way alongside your components, rather than having to maintain separate style sheets. Here's an example of using Styled Components in a React component:

```jsx
import styled from "styled-components";

const Button = styled.button`
  background: palevioletred;
  border-radius: 3px;
  border: none;
  color: white;
`;

function MyComponent() {
  return <Button>Click me!</Button>;
}
```

One advantage of Styled Components is that it helps to keep your styles organized and modular. Instead of having a separate CSS file for each component, you can define the styles directly within the component itself. This can make it easier to understand and maintain your code, as everything related to the component is kept in one place.

Styled Components also allows you to easily customize your styles based on props passed to the component, and to define complex styles using standard CSS syntax.

However, Styled Components does require an additional library to be installed and imported, which can add some complexity to your project. It may also have a slightly higher learning curve for developers who are not familiar with CSS-in-JS libraries.

Ultimately, the choice between inline styling and Styled Components will depend on your specific needs and preferences. If you're looking for a quick and easy way to apply simple styles, inline styling may be the way to go. If you want more control and flexibility over your styles, and are willing to invest some time in learning a new library, Styled Components may be a better choice.

</details>

## React Coding Interview Questions

<details>
<summary>
    <h3>53. What is the output of the following code snippet when the "Click me" button is clicked twice?
 </h3>

```jsx
function App() {
  const [count, setCount] = React.useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

</summary>

### Answer

The output would be "You clicked 2 times".

</details>

<details>
<summary>
    <h3>54. What is the output of the following code snippet when the "Increment age" button is clicked three times?
 </h3>

```jsx
function App() {
  const [state, setState] = React.useState({
    name: "John",
    age: 30,
  });

  return (
    <div>
      <p>
        My name is {state.name} and I am {state.age} years old
      </p>
      <button onClick={() => setState({ ...state, age: state.age + 1 })}>
        Increment age
      </button>
    </div>
  );
}
```

</summary>

### Answer

The output would be "My name is John and I am 33 years old".

</details>

<details>
<summary>
    <h3>55. What is the output of the following code snippet when the "Add hobby" button is clicked twice and then the page is refreshed?
 </h3>

```jsx
function App() {
  const [state, setState] = React.useState({
    name: "John",
    age: 30,
    hobbies: ["reading", "running"],
  });

  return (
    <div>
      <p>
        My name is {state.name} and I am {state.age} years old
      </p>
      <ul>
        {state.hobbies.map((hobby) => (
          <li key={hobby}>{hobby}</li>
        ))}
      </ul>
      <button
        onClick={() =>
          setState({ ...state, hobbies: [...state.hobbies, "swimming"] })
        }
      >
        Add hobby
      </button>
    </div>
  );
}
```

</summary>

### Answer

The output would be a list with two items: "reading" and "running". The state of the component is reset when the page is refreshed, so the hobbies list would only contain the original two items after the refresh.

</details>

<details>
<summary>
    <h3>56. What is the output of the following code snippet when the "Increment" button is clicked twice and then the "Reset" button is clicked once?
 </h3>

```jsx
import { useEffect, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("count updated");
  }, []);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(0)}>Reset</button>
    </div>
  );
}
```

 </summary>
Answer
The output would be:

```jsx
count updated
```

The `useEffect` hook is called every time the component is rendered, but the dependencies array is empty. This means that the effect will only be run on the initial render of the component, and not on subsequent renders. Since the `Increment` button is clicked twice and the component is re-rendered each time, the effect is not run. However, when the `Reset` button is clicked and the component is re-rendered with a new value for count, the effect is run and the string `count updated` is logged to the console.

</details>

<details>
<summary>
    <h3>57. Create your own useState hook for your new vanilla javascript project.
 </h3>
 </summary>
Here is an example of a `useState` hook function that you can use in a `vanilla` JavaScript project:

```jsx
function useState(initialState) {
  let state = initialState;
  function setState(newState) {
    //we can also add few conditions to validate the data.
    state = newState;
    render(); //your custom method to trigger page refresh on state change
  }
  return [state, setState];
}
```

Here is an example of a `useState` hook which might be implemented in a vanilla JavaScript project.

The useState function takes an `initial state` as an argument, and returns an array with the current state and a function to update it.

The state is maintained in a `closure` so that it can be accessed and updated by the component functions.

For the render function on the setState is not something that you would typically include in a vanilla implementation, since is related to some kind of framework, but in your case you may replace it with your specific render function.

</details>

<details>
<summary>
    <h3>58. Write a custom hook which can be used to apply dark or light mode.
 </h3>

 </summary>

```jsx
//custom hook

const useDarkMode = () => {
  const [isDarkMode, setIsDarkMode] = useState(
    localStorage.getItem("isDarkMode") === "true"
  );

  // function to toggle
  const toggleDarkMode = () => {
    setIsDarkMode((prevMode) => {
      localStorage.setItem("isDarkMode", !prevMode);
      return !prevMode;
    });
  };
  return { isDarkMode, toggleDarkMode };
};

export default useDarkMode;
```

```jsx
//usage
// note- there should be different classes to toggle between dark and light mode
// here, ex- 'dark-mode', 'light-mode'

const App = () => {
  const { isDarkMode, toggleDarkMode } = useDarkMode();

  return (
    <div className={isDarkMode ? "dark-mode" : "light-mode"}>
      <button onClick={toggleDarkMode}>
        {isDarkMode ? "Switch to Light Mode" : "Switch to Dark Mode"}
      </button>
    </div>
  );
};
export default App;
```

Here's an example of a custom hook that can toggle between dark and light mode, and also uses local storage to persist the theme across different sessions in a single file.

This is a simple example, you can improve this by adding more styles, and you can also use it in multiple components.

</details>

<details>
<summary>
    <h3>59. How to access the latest value of a text input field in a React component using the 'useRef' hook?
 </h3>

 </summary>

Answer:

You can access the latest value of a text input field in a React component using the `useRef` hook as follows:

```jsx
import React, { useRef } from "react";

const InputComponent = () => {
  const inputRef = useRef(null);

  const handleClick = () => {
    console.log(inputRef.current.value);
  };

  return (
    <div>
      <input type="text" ref={inputRef} />
      <button onClick={handleClick}>Show value </button>
    </div>
  );
};
```

</details>

<details>
<summary>
    <h3>60. How to create a counter that increments every second using the 'useRef' hook?
 </h3>

 </summary>

Answer:

You can create a counter that increments every second using the `useRef` hook as follows:

```jsx
import React, { useState, useRef, useEffect } from "react";

const Counter = () => {
  const [count, setCount] = useState(0);
  const intervalRef = useRef();

  useEffect(() => {
    intervalRef.current = setInterval(() => {
      setCount((count) => count + 1);
    }, 1000);

    return () => {
      clearInterval(intervalRef.current);
    };
  }, []);

  return <h1>{count}</h1>;
};
```

</details>

<details>
<summary>
    <h3>61. How to implement a simple dropdown menu using the 'useRef' hook?
 </h3>

 </summary>

Answer:

You can implement a simple dropdown menu using the `useRef` hook as follows:

```jsx
import React, { useState, useRef } from "react";

const Dropdown = () => {
  const [isOpen, setIsOpen] = useState(false);
  const dropdownRef = useRef(null);

  const handleClickOutside = (event) => {
    if (dropdownRef.current && !dropdownRef.current.contains(event.target)) {
      setIsOpen(false);
    }
  };

  useEffect(() => {
    document.addEventListener("mousedown", handleClickOutside);
    return () => {
      document.removeEventListener("mousedown", handleClickOutside);
    };
  }, []);

  return (
    <div ref={dropdownRef}>
      <button onClick={() => setIsOpen(!isOpen)}>Dropdown</button>
      {isOpen && (
        <ul>
          <li>Option 1</li>
          <li>Option 2</li>
          <li>Option 3</li>
        </ul>
      )}
    </div>
  );
};
```

</details>

<details>
<summary>
    <h3>62. Can you explain the React architecture in one sentence?</h3>

```bash
Think You Know React? Try Answering this!
```

</summary>
Answer:

React is like a virtual Lego set where each component is a brick that can be combined in various ways to build complex user interfaces.

</details>
<details>
<summary>
    <h3>63. How does React know what to render?</h3>

```bash
Think You Know React? Try Answering this!
```

</summary>
Answer:

React uses a virtual DOM to keep track of the state of the application and determine what changes need to be made to the real DOM to reflect those changes.

</details>

<details>
<summary>
    <h3>64. If React was a food, what food would it be?</h3>

```bash
Think You Know React? Try Answering this!
```

</summary>
Answer:

React would be like a sushi platter, where each piece of sushi is a component and can be combined in different ways to create a unique and satisfying user experience.

</details>

<details>
<summary>
    <h3>65. How would you explain the concept of "lifting state up" in React?</h3>
</summary>
Answer:

Lifting state up is the process of moving state from a lower-level component to a higher-level component in the React component hierarchy.

This is done to share state between sibling components that do not have a direct parent-child relationship.

By lifting state up to a common ancestor component, we can avoid prop drilling and make the application more efficient and easier to maintain.

```jsx
import React, { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  const incrementCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h1>Count: {count}</h1>
      <CounterButton incrementCount={incrementCount} />
      <ResetButton setCount={setCount} />
    </div>
  );
}

function CounterButton({ incrementCount }) {
  return <button onClick={incrementCount}>Increment Count</button>;
}

function ResetButton({ setCount }) {
  return <button onClick={() => setCount(0)}>Reset Count</button>;
}
```

By lifting the count state up to the App component, we can share this state between the CounterButton and ResetButton components without having to pass it down as props through multiple levels of components.

This makes the code cleaner and more efficient, and avoids prop drilling.

</details>

<details>
<summary>
    <h3>66. How does Next.js differ from React.js, and what benefits does it provide for building web applications?</h3>
</summary>
Answer:

Next.js is a framework built on top of React.js that provides additional features for building server-side rendered web applications.

One of the main differences between Next.js and React.js is that Next.js provides server-side rendering out of the box, which allows for faster initial page loads and better search engine optimization.

Next.js also provides features like automatic code splitting and optimized performance for production builds, which can make it easier to build and deploy large-scale applications.

Additionally, Next.js provides support for static site generation, which allows for even faster load times and improved user experiences.

Overall, Next.js provides a more complete solution for building modern web applications than React.js alone, and can be especially beneficial for larger applications that require server-side rendering and other advanced features.

</details>

## React Js Coding Test Questions and Qnswers

<details>
<summary>
    <h3>67. Scenario Based - </h3>
    
You have been tasked with creating a form component that allows users to submit data to an API endpoint using React. The form should include the following fields:

```bash
Name (required)
Email (required)
Message (required)
Checkbox (optional)
```

When the user submits the form, the data should be sent to the API endpoint as a POST request. If the request is successful, the form should be reset and a success message should be displayed. If the request fails, an error message should be displayed.

Write a functional React component that implements the above requirements.

</summary>
Answer:

```jsx
import React, { useState } from "react";

function ContactForm() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    message: "",
    checkbox: false,
  });
  const [submitting, setSubmitting] = useState(false);
  const [submitted, setSubmitted] = useState(false);
  const [error, setError] = useState("");

  const handleChange = (e) => {
    const { name, value, checked } = e.target;
    setFormData({
      ...formData,
      [name]: name === "checkbox" ? checked : value,
    });
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    setSubmitting(true);

    try {
      const response = await fetch("https://example.com/api/contact", {
        method: "POST",
        body: JSON.stringify(formData),
        headers: {
          "Content-Type": "application/json",
        },
      });
      if (!response.ok) {
        throw new Error("Error submitting form");
      }
      setFormData({
        name: "",
        email: "",
        message: "",
        checkbox: false,
      });
      setSubmitted(true);
      setError("");
    } catch (err) {
      setError(err.message);
    } finally {
      setSubmitting(false);
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <label htmlFor="name">Name</label>
      <input
        type="text"
        id="name"
        name="name"
        value={formData.name}
        onChange={handleChange}
        required
      />

      <label htmlFor="email">Email</label>
      <input
        type="email"
        id="email"
        name="email"
        value={formData.email}
        onChange={handleChange}
        required
      />

      <label htmlFor="message">Message</label>
      <textarea
        id="message"
        name="message"
        value={formData.message}
        onChange={handleChange}
        required
      />

      <label htmlFor="checkbox">
        <input
          type="checkbox"
          id="checkbox"
          name="checkbox"
          checked={formData.checkbox}
          onChange={handleChange}
        />
        Checkbox
      </label>

      {error && <div>{error}</div>}
      {submitting ? (
        <div>Submitting...</div>
      ) : submitted ? (
        <div>Form submitted successfully!</div>
      ) : (
        <button type="submit">Submit</button>
      )}
    </form>
  );
}

export default ContactForm;
```

This form component uses the useState hook to manage the form data, submission status, and error state. When the form is submitted, it sends a POST request to the specified API endpoint using fetch(), and displays either a success message, an error message, or a loading spinner depending on the submission status.

</details>

<details>
<summary>
    <h3>68. Scenario Based - </h3>
    
You have been given a requirement to build a simple to-do list application in React. The application should allow the user to add, edit, and delete tasks from the list. Each task should have a title, a description, and a priority level (high, medium, low). When a task is marked as completed, it should be displayed with a strikethrough.

Write a React component that implements the above requirements. You may use any state management library of your choice (e.g. Redux, MobX, Context API).

</summary>
Answer:

```jsx
import React, { useState } from "react";

function TodoList() {
  const [tasks, setTasks] = useState([]);

  const [newTask, setNewTask] = useState({
    title: "",
    description: "",
    priority: "medium",
    completed: false,
  });

  const handleNewTaskChange = (e) => {
    const { name, value } = e.target;
    setNewTask({
      ...newTask,
      [name]: value,
    });
  };

  const handleAddTask = (e) => {
    e.preventDefault();
    setTasks([...tasks, newTask]);
    setNewTask({
      title: "",
      description: "",
      priority: "medium",
      completed: false,
    });
  };

  const handleDeleteTask = (index) => {
    const newTasks = [...tasks];
    newTasks.splice(index, 1);
    setTasks(newTasks);
  };

  const handleEditTask = (index, updatedTask) => {
    const newTasks = [...tasks];
    newTasks[index] = updatedTask;
    setTasks(newTasks);
  };

  const toggleCompleted = (index) => {
    const newTasks = [...tasks];
    newTasks[index].completed = !newTasks[index].completed;
    setTasks(newTasks);
  };

  return (
    <div>
      <form onSubmit={handleAddTask}>
        <input
          type="text"
          name="title"
          placeholder="Task title"
          value={newTask.title}
          onChange={handleNewTaskChange}
        />
        <textarea
          name="description"
          placeholder="Task description"
          value={newTask.description}
          onChange={handleNewTaskChange}
        />
        <select
          name="priority"
          value={newTask.priority}
          onChange={handleNewTaskChange}
        >
          <option value="high">High</option>
          <option value="medium">Medium</option>
          <option value="low">Low</option>
        </select>
        <button type="submit">Add Task</button>
      </form>

      <ul>
        {tasks.map((task, index) => (
          <li key={index}>
            <h3
              style={{
                textDecoration: task.completed ? "line-through" : "none",
              }}
            >
              {task.title}
            </h3>
            <p>{task.description}</p>
            <div>
              <button onClick={() => handleDeleteTask(index)}>Delete</button>
              <button onClick={() => toggleCompleted(index)}>
                {task.completed ? "Mark Incomplete" : "Mark Complete"}
              </button>
              <button
                onClick={() => {
                  const updatedTask = prompt("Enter updated task:");
                  if (updatedTask) {
                    handleEditTask(index, {
                      ...task,
                      title: updatedTask,
                    });
                  }
                }}
              >
                Edit
              </button>
            </div>
          </li>
        ))}
      </ul>
    </div>
  );
}

export default TodoList;
```

</details>

<details>
<summary>
    <h3>69. Scenario Based - </h3>

You have been assigned to create a registration form component in React. The form should include fields for the user to enter their name, email, and password.

Implement form validation to ensure that the following conditions are met:

- The name field is required and should contain only alphabetic characters.
- The email field is required and should be a valid email address format.
- The password field is required and should have a minimum length of 8 characters.

Write a React component that implements the above requirements.

</summary>

Solution -

```jsx
import React, { useState } from "react";

function RegistrationForm() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    password: "",
  });

  const [errors, setErrors] = useState({
    name: "",
    email: "",
    password: "",
  });

  const handleInputChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value,
    });
  };

  const validateForm = () => {
    let isValid = true;
    const newErrors = {
      name: "",
      email: "",
      password: "",
    };

    if (formData.name.trim() === "") {
      newErrors.name = "Name is required";
      isValid = false;
    } else if (!/^[a-zA-Z]+$/.test(formData.name)) {
      newErrors.name = "Name should only contain alphabetic characters";
      isValid = false;
    }

    if (formData.email.trim() === "") {
      newErrors.email = "Email is required";
      isValid = false;
    } else if (
      !/^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i.test(formData.email)
    ) {
      newErrors.email = "Invalid email address";
      isValid = false;
    }

    if (formData.password.trim() === "") {
      newErrors.password = "Password is required";
      isValid = false;
    } else if (formData.password.length < 8) {
      newErrors.password = "Password should be at least 8 characters long";
      isValid = false;
    }

    setErrors(newErrors);
    return isValid;
  };

  const handleSubmit = (e) => {
    e.preventDefault();

    if (validateForm()) {
      // Form is valid, proceed with registration logic
      // e.g., submit data to server or perform necessary actions
      console.log("Form submitted successfully:", formData);
    }
  };

  return (
    <div>
      <h2>Registration Form</h2>
      <form onSubmit={handleSubmit}>
        <div>
          <label>Name:</label>
          <input
            type="text"
            name="name"
            value={formData.name}
            onChange={handleInputChange}
          />
          {errors.name && <span>{errors.name}</span>}
        </div>

        <div>
          <label>Email:</label>
          <input
            type="email"
            name="email"
            value={formData.email}
            onChange={handleInputChange}
          />
          {errors.email && <span>{errors.email}</span>}
        </div>

        <div>
          <label>Password:</label>
          <input
            type="password"
            name="password"
            value={formData.password}
            onChange={handleInputChange}
          />
          {errors.password && <span>{errors.password}</span>}
        </div>

        <button type="submit">Register</button>
      </form>
    </div>
  );
}

export default RegistrationForm;
```

The component uses React hooks to manage form data and validation errors.

The form fields include name, email, and password, and the component ensures that each field meets the specified validation criteria before allowing form submission.

</details>

<details>
<summary>
<h3>70. Scenario Based - Controlled Input with Delayed Value Display</h3>

Create a React component that consists of an input field.

The component should be controlled, meaning its value is determined by React state.

However, when the user types in the input field, there should be a 2-second delay before the displayed value updates.

If the user types new characters within this 2-second interval, the display update should be delayed again by 2 seconds.

Only after 2 seconds of inactivity, the displayed value should be updated with the latest input.

Implement the above behavior in the React component.

</summary>

Solution -

```jsx
import React, { useState, useEffect } from "react";

function DelayedInput() {
  const [inputValue, setInputValue] = useState("");
  const [displayValue, setDisplayValue] = useState("");

  useEffect(() => {
    let timeoutId = null;

    // Update the display value after a 2-second delay
    const delayedUpdateDisplay = () => {
      timeoutId = setTimeout(() => {
        setDisplayValue(inputValue);
      }, 2000);
    };

    // Clear the previous timeout when the user types within 2 seconds
    clearTimeout(timeoutId);

    // Initiate the delayed update only when the user stops typing
    delayedUpdateDisplay();

    // Clean up the timeout on component unmount
    return () => {
      clearTimeout(timeoutId);
    };
  }, [inputValue]);

  const handleInputChange = (e) => {
    setInputValue(e.target.value);
  };

  return (
    <div>
      <h2>Delayed Input</h2>
      <input type="text" value={inputValue} onChange={handleInputChange} />
      <p>Display Value: {displayValue}</p>
    </div>
  );
}

export default DelayedInput;
```

The component `DelayedInput` uses React hooks such as `useEffect` to achieve the delayed value display functionality. As the user types, the `inputValue` state is updated immediately, but the displayed value (`displayValue`) is updated after a 2-second delay.

</details>

<details>
<summary>
<h3>71. Scenario Based - Dynamic Nested List Rendering</h3>

Create a React component that renders a nested list from a given array of objects. Each object can have a `name` property and a nested `children` property, which is an array of objects with the same structure.

The depth of nesting is unknown and can vary for different objects.

Implement the React component to render the nested list based on the provided data.

Example Data:

```jsx
const data = [
  {
    name: "Item 1",
    children: [
      {
        name: "Subitem 1.1",
        children: [
          { name: "Subsubitem 1.1.1", children: [] },
          { name: "Subsubitem 1.1.2", children: [] },
        ],
      },
      { name: "Subitem 1.2", children: [] },
    ],
  },
  {
    name: "Item 2",
    children: [
      { name: "Subitem 2.1", children: [] },
      { name: "Subitem 2.2", children: [] },
    ],
  },
];
```

Render the nested list using the provided data.

</summary>

Solution -

```jsx
import React from "react";

function NestedList({ data }) {
  const renderNestedItems = (items) => {
    return (
      <ul>
        {items.map((item, index) => (
          <li key={index}>
            {item.name}
            {item.children.length > 0 && renderNestedItems(item.children)}
          </li>
        ))}
      </ul>
    );
  };

  return (
    <div>
      <h2>Nested List</h2>
      {renderNestedItems(data)}
    </div>
  );
}

export default NestedList;
```

The component `NestedList` recursively renders a nested list using the provided `data` prop. It checks if the current item has children and, if so, calls the `renderNestedItems` function recursively to render the nested list.

</details>

<details>
<summary>
<h3>72. Scenario Based - Async Data Fetch and Rendering</h3>

Create a React component that fetches data from a given API endpoint and renders it as a list.

The API endpoint returns an array of objects, each containing an `id` and a `name`. However, there is a 2-second delay before the API responds.

Implement the React component to fetch the data from the API and display it as a list.

API Endpoint: `https://jsonplaceholder.typicode.com/users`

</summary>

Solution -

```jsx
import React, { useState, useEffect } from "react";

function DataList() {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch(
          "https://jsonplaceholder.typicode.com/users"
        );
        const json = await response.json();
        // Simulate a 2-second delay before setting the data
        setTimeout(() => {
          setData(json);
          setLoading(false);
        }, 2000);
      } catch (error) {
        console.error("Error fetching data:", error);
        setLoading(false);
      }
    };

    fetchData();
  }, []);

  return (
    <div>
      <h2>Data List</h2>
      {loading ? (
        <p>Loading...</p>
      ) : (
        <ul>
          {data.map((item) => (
            <li key={item.id}>{item.name}</li>
          ))}
        </ul>
      )}
    </div>
  );
}

export default DataList;
```

The component `DataList` uses `useEffect` hook to fetch data from the provided API endpoint.

While waiting for the API response, it displays a loading message. After a 2-second delay (simulated using `setTimeout`), the fetched data is rendered as a list.

</details>

<details>
<summary>
<h3>73. Scenario Based - Managing Focus with useRef</h3>

Create a React component that includes an input field and a button. When the button is clicked, it should focus on the input field.

Implement this functionality using the `useRef` hook.

</summary>

Solution:

```jsx
import React, { useRef } from "react";

function FocusInput() {
  const inputRef = useRef(null);

  const handleFocusButtonClick = () => {
    // Focus on the input field
    if (inputRef.current) {
      inputRef.current.focus();
    }
  };

  return (
    <div>
      <h2>Focus Input</h2>
      <input ref={inputRef} type="text" placeholder="Enter text" />
      <button onClick={handleFocusButtonClick}>Focus Input</button>
    </div>
  );
}

export default FocusInput;
```

In this component, we use the `useRef` hook to create a reference (`inputRef`) to the input element. When the button is clicked, the `handleFocusButtonClick` function is called, and it focuses on the input element by calling `inputRef.current.focus()`. This allows us to programmatically manage the focus of the input field.

</details>

<details>
<summary>
<h3>74. What is a higher-order component in React?</h3>

A higher-order component acts as a container for other components. This helps to keep components simple and enables re-usability. They are generally used when multiple components have to use a common logic.

</summary>

Solution:

```jsx
import React, { useState, useEffect } from "react";

const CommentList = () => {
  const [comments, setComments] = useState(DataSource.getComments());

  useEffect(() => {
    const handleChange = () => {
      setComments(DataSource.getComments());
    };

    // Subscribe to changes
    DataSource.addChangeListener(handleChange);

    // Clean up listener
    return () => {
      DataSource.removeChangeListener(handleChange);
    };
  }, []); // Empty dependency array to mimic componentDidMount and componentWillUnmount

  return (
    <div>
      {comments.map((comment) => (
        <Comment comment={comment} key={comment.id} />
      ))}
    </div>
  );
};

export default CommentList;
```

The CommentList component is a React functional component that displays a list of comments. It utilizes the useState hook to manage the comments state and the useEffect hook to subscribe to changes in a global data source (DataSource). When the component mounts, it fetches initial comments and sets up a change listener, updating the state whenever the data source changes. The component renders a list of Comment components based on the comments in its state, each uniquely identified by its id. The change listener is removed when the component unmounts to avoid memory leaks.

</details>

<details>
<summary>
<h3>75. Explain the role of keys in React lists and the potential issues that can arise without them. Provide a code example to demonstrate their usage.</h3>
</summary>

**Answer:**

Keys in React lists serve a crucial purpose for efficient rendering and reconciliation.

They enable React to identify which items in a list have changed, been added, or removed, and update the DOM accordingly.

**Without keys, React may perform unnecessary re-renders of components, leading to performance issues and potential bugs.**

Here are key points to remember:

- **Uniqueness:** Each item in a list should have a unique key.
- **Stability:** Keys should remain consistent across re-renders unless the items themselves change identity.
- **Data Attributes:** Using data attributes from the items themselves is often a good approach for key assignment.

**Example:**

```jsx
import React from "react";

const TodoList = ({ todos }) => {
  return (
    <ul>
      {todos.map((todo, index) => (
        <li key={todo.id}>{todo.text}</li>
      ))}
    </ul>
  );
};
```

**Explanation:**

- The `TodoList` component renders a list of `Todo` items.
- Each `Todo` item is assigned a unique key using its `id` property.
- React uses these keys to track changes and apply updates efficiently.

</details>

<details>
<summary>
<h3>76. Scenario Based - Browser's Local Storage</h3>

Imagine you are working on a task management application using React. You want to implement a feature where the user's tasks are saved locally so that even if they refresh the page or close the browser, their tasks remain intact.

How would you achieve this using local storage in React?

</summary>

Solution:

```jsx
import React, { useState, useEffect } from "react";
import TaskList from "./TaskList";

const App = () => {
  const [tasks, setTasks] = useState([]);

  useEffect(() => {
    const storedTasks = localStorage.getItem("tasks");
    if (storedTasks) {
      setTasks(JSON.parse(storedTasks));
    }
  }, []);

  useEffect(() => {
    localStorage.setItem("tasks", JSON.stringify(tasks));
  }, [tasks]);

  const addTask = (newTask) => {
    setTasks([...tasks, newTask]);
  };

  const deleteTask = (taskId) => {
    const updatedTasks = tasks.filter((task) => task.id !== taskId);
    setTasks(updatedTasks);
  };

  return (
    <div className="App">
      <h1>Task Management App</h1>
      <TaskList tasks={tasks} addTask={addTask} deleteTask={deleteTask} />
    </div>
  );
};

export default App;
```

In this component, tasks are stored in local storage under the key 'tasks', and they are loaded into the state when the component mounts. Changes to the tasks state are automatically synced with local storage using another useEffect hook.

</details>

<details>
<summary>
<h3>77. Scenario Based - Browser's Session Storage</h3>

Imagine you are developing a shopping cart feature for an e-commerce website using React. You want to implement a feature where the user's cart items are saved temporarily during their session. If they navigate away from the cart page and come back, their cart items should still be there, but if they close the browser, the cart should be reset.

How would you achieve this using session storage in React?

</summary>

Solution:

```jsx
import React, { useState, useEffect } from "react";
import Cart from "./Cart";

const App = () => {
  const [cartItems, setCartItems] = useState([]);

  useEffect(() => {
    const storedCartItems = sessionStorage.getItem("cartItems");
    if (storedCartItems) {
      setCartItems(JSON.parse(storedCartItems));
    }
  }, []);

  useEffect(() => {
    sessionStorage.setItem("cartItems", JSON.stringify(cartItems));
  }, [cartItems]);

  const addItemToCart = (newItem) => {
    setCartItems([...cartItems, newItem]);
  };

  const removeItemFromCart = (itemId) => {
    const updatedCartItems = cartItems.filter((item) => item.id !== itemId);
    setCartItems(updatedCartItems);
  };

  return (
    <div className="App">
      <h1>Shopping Cart</h1>
      <Cart
        cartItems={cartItems}
        addItemToCart={addItemToCart}
        removeItemFromCart={removeItemFromCart}
      />
    </div>
  );
};

export default App;
```

In this component, cart items are stored in session storage under the key 'cartItems', and they are loaded into the state when the component mounts. Changes to the cartItems state are automatically synced with session storage using another useEffect hook.

</details>

<details>
<summary>
<h3>78. Scenario Based - Async Data Fetch with Caching and Error Handling</h3>

Create a React component that fetches and displays a list of users from an API endpoint.

### Requirements:

- Fetch data from the API endpoint when the component mounts.
- Implement a caching mechanism to prevent unnecessary API calls if the data is already available.
- Show a loading state while fetching data.
- Handle API errors gracefully and display a retry button.
- Ensure efficient re-renders and avoid unnecessary re-fetching.

API Endpoint: `https://jsonplaceholder.typicode.com/users`

</summary>

Solution -

```jsx
import React, { useState, useEffect } from "react";

const cache = {}; // Simple in-memory cache

function UserList() {
  const [data, setData] = useState(cache.users || []);
  const [loading, setLoading] = useState(!cache.users);
  const [error, setError] = useState(null);

  const fetchData = async () => {
    if (cache.users) return; // Use cached data if available

    setLoading(true);
    setError(null);
    try {
      const response = await fetch(
        "https://jsonplaceholder.typicode.com/users"
      );

      if (!response.ok) throw new Error("Failed to fetch data");

      const json = await response.json();
      cache.users = json; // Store data in cache
      setData(json);
    } catch (err) {
      setError(err.message);
    } finally {
      setLoading(false);
    }
  };

  useEffect(() => {
    fetchData();
  }, []);

  return (
    <div>
      <h2>User List</h2>
      {loading && <p>Loading...</p>}
      {error && (
        <div>
          <p>Error: {error}</p>
          <button onClick={fetchData}>Retry</button>
        </div>
      )}
      {!loading && !error && (
        <ul>
          {data.map((user) => (
            <li key={user.id}>{user.name}</li>
          ))}
        </ul>
      )}
    </div>
  );
}

export default UserList;
```

### Explanation:

- The component first checks if data is available in the cache to avoid unnecessary API calls.
- If no cached data exists, it fetches data from the API and caches it.
- Displays a loading state while fetching.
- Handles errors gracefully by showing an error message and a retry button.
- Ensures the UI only updates when necessary, optimizing performance.

This question evaluates:  
✅ Optimized data fetching with caching  
✅ Proper error handling and retry mechanisms  
✅ Efficient re-renders to prevent unnecessary API calls

</details>

---

## React 19 Features & Modern React

<details>
<summary>
    <h3>79. What are the new features introduced in React 19?</h3>
</summary>

React 19 introduces several powerful features that enhance developer experience and application performance:

**New Hooks:**

- **`use()` Hook**: A new hook that can consume promises and context
- **`useFormStatus()`**: For handling form submission states
- **`useActionState()`**: For managing server actions state

**React Compiler (Automatic Memoization):**

- Automatically optimizes your components without manual memoization
- Eliminates the need for `useMemo`, `useCallback`, and `React.memo` in many cases

**Server Components Enhancements:**

- Improved Server Components with better hydration
- Enhanced streaming capabilities
- Better integration with frameworks like Next.js

**Actions and Forms:**

- Native support for Server Actions
- Improved form handling with automatic pending states
- Built-in error boundaries for async operations

```tsx
// React 19 - use() hook example
import { use } from "react";

interface User {
  id: number;
  name: string;
}

function UserProfile({ userPromise }: { userPromise: Promise<User> }) {
  const user = use(userPromise);

  return <div>Welcome, {user.name}!</div>;
}

// React 19 - useFormStatus() example
import { useFormStatus } from "react-dom";

function SubmitButton() {
  const { pending } = useFormStatus();

  return (
    <button type="submit" disabled={pending}>
      {pending ? "Submitting..." : "Submit"}
    </button>
  );
}
```

</details>

<details>
<summary>
    <h3>80. Explain React's new `use()` hook and provide examples.</h3>
</summary>

The `use()` hook is a new primitive in React 19 that can consume promises and context. Unlike other hooks, `use()` can be called conditionally.

**Key Features:**

- Can consume Promises and Context
- Can be called conditionally (unlike other hooks)
- Suspends the component while waiting for Promise resolution

```tsx
import { use, Suspense } from "react";

// TypeScript interfaces
interface User {
  id: number;
  name: string;
  email: string;
}

// Consuming a Promise with use()
function UserData({ userPromise }: { userPromise: Promise<User> }) {
  const user = use(userPromise);

  return (
    <div>
      <h2>{user.name}</h2>
      <p>{user.email}</p>
    </div>
  );
}

// Consuming Context with use()
import { createContext } from "react";

const ThemeContext = createContext<"light" | "dark">("light");

function ThemeDisplay() {
  const theme = use(ThemeContext);

  return <div>Current theme: {theme}</div>;
}

// Usage with conditional logic
function ConditionalData({
  shouldFetch,
  dataPromise,
}: {
  shouldFetch: boolean;
  dataPromise: Promise<any>;
}) {
  if (!shouldFetch) {
    return <div>Not fetching data</div>;
  }

  // This is allowed with use() but not with other hooks
  const data = use(dataPromise);
  return <div>{data.content}</div>;
}

// App component
function App() {
  const userPromise = fetch("/api/user").then((res) => res.json());

  return (
    <Suspense fallback={<div>Loading...</div>}>
      <UserData userPromise={userPromise} />
    </Suspense>
  );
}
```

</details>

<details>
<summary>
    <h3>81. What is the React Compiler and how does it improve performance?</h3>
</summary>

The React Compiler is an experimental feature in React 19 that automatically optimizes React components by adding memoization where beneficial, eliminating the need for manual optimization with `useMemo`, `useCallback`, and `React.memo`.

**Key Benefits:**

- **Automatic Optimization**: No manual memoization needed
- **Better Performance**: Prevents unnecessary re-renders automatically
- **Developer Experience**: Focus on logic, not performance optimization
- **Gradual Adoption**: Can be enabled incrementally

```tsx
// Before React Compiler (Manual optimization)
import { useMemo, useCallback, memo } from "react";

interface User {
  id: number;
  name: string;
}

interface TodoListProps {
  users: User[];
  onUserSelect: (userId: number) => void;
}

const TodoList = memo(({ users, onUserSelect }: TodoListProps) => {
  const expensiveComputation = useMemo(() => {
    return users
      .filter((user) => user.name.length > 5)
      .map((user) => ({ ...user, displayName: user.name.toUpperCase() }));
  }, [users]);

  const handleUserClick = useCallback(
    (userId: number) => {
      onUserSelect(userId);
    },
    [onUserSelect]
  );

  return (
    <div>
      {expensiveComputation.map((user) => (
        <div key={user.id} onClick={() => handleUserClick(user.id)}>
          {user.displayName}
        </div>
      ))}
    </div>
  );
});

// After React Compiler (Automatic optimization)
function TodoList({ users, onUserSelect }: TodoListProps) {
  // React Compiler automatically memoizes this computation
  const expensiveComputation = users
    .filter((user) => user.name.length > 5)
    .map((user) => ({ ...user, displayName: user.name.toUpperCase() }));

  // React Compiler automatically memoizes this callback
  const handleUserClick = (userId: number) => {
    onUserSelect(userId);
  };

  return (
    <div>
      {expensiveComputation.map((user) => (
        <div key={user.id} onClick={() => handleUserClick(user.id)}>
          {user.displayName}
        </div>
      ))}
    </div>
  );
}
```

**How to enable React Compiler:**

```bash
# Install React Compiler
npm install react-compiler-runtime
npm install --save-dev babel-plugin-react-compiler
```

</details>

<details>
<summary>
    <h3>82. What are React Server Components and how do they work?</h3>
</summary>

React Server Components (RSC) are components that run on the server and send their rendered output to the client. They enable better performance by reducing the JavaScript bundle size and improving initial page load.

**Key Benefits:**

- **Zero Bundle Size**: Server Components don't add to client bundle
- **Direct Server Access**: Can directly access databases, file systems
- **Automatic Code Splitting**: Only client components are bundled
- **SEO Friendly**: Pre-rendered on server

```tsx
// Server Component (runs on server)
import { db } from "@/lib/database";

interface BlogPost {
  id: string;
  title: string;
  content: string;
  author: string;
}

// This component runs on the server
async function BlogList() {
  // Direct database access - only runs on server
  const posts: BlogPost[] = await db.posts.findMany({
    orderBy: { createdAt: "desc" },
  });

  return (
    <div className="blog-list">
      <h1>Latest Blog Posts</h1>
      {posts.map((post) => (
        <article key={post.id}>
          <h2>{post.title}</h2>
          <p>By {post.author}</p>
          <div>{post.content.substring(0, 200)}...</div>
        </article>
      ))}
    </div>
  );
}

// Client Component (runs in browser)
("use client");

import { useState } from "react";

interface SearchBarProps {
  onSearch: (query: string) => void;
}

function SearchBar({ onSearch }: SearchBarProps) {
  const [query, setQuery] = useState("");

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    onSearch(query);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={query}
        onChange={(e) => setQuery(e.target.value)}
        placeholder="Search posts..."
      />
      <button type="submit">Search</button>
    </form>
  );
}

// Layout combining Server and Client Components
function BlogPage() {
  return (
    <div>
      {/* This runs on the client for interactivity */}
      <SearchBar onSearch={(query) => console.log(query)} />

      {/* This runs on the server for data fetching */}
      <BlogList />
    </div>
  );
}
```

**File Structure Example:**

```
app/
├── layout.tsx          // Server Component
├── page.tsx           // Server Component
├── blog/
│   ├── page.tsx       // Server Component
│   └── search.tsx     // Client Component ('use client')
└── components/
    ├── header.tsx     // Server Component
    └── interactive.tsx // Client Component
```

</details>

<details>
<summary>
    <h3>83. Explain the App Router in Next.js 13+ and its benefits.</h3>
</summary>

The App Router is a new routing system in Next.js 13+ that leverages React Server Components and provides a more intuitive file-based routing system.

**Key Features:**

- **File-based routing** with `app/` directory
- **Layouts** and **Templates** for shared UI
- **Server Components** by default
- **Streaming** and **Suspense** support
- **Parallel Routes** and **Intercepting Routes**

```tsx
// app/layout.tsx - Root Layout (Server Component)
import "./globals.css";

export const metadata = {
  title: "My App",
  description: "A Next.js 13+ application",
};

interface RootLayoutProps {
  children: React.ReactNode;
}

export default function RootLayout({ children }: RootLayoutProps) {
  return (
    <html lang="en">
      <body>
        <header>
          <nav>My Navigation</nav>
        </header>
        <main>{children}</main>
        <footer>My Footer</footer>
      </body>
    </html>
  );
}

// app/page.tsx - Home Page (Server Component)
export default function HomePage() {
  return (
    <div>
      <h1>Welcome to My App</h1>
      <p>This is a server component!</p>
    </div>
  );
}

// app/blog/layout.tsx - Nested Layout
interface BlogLayoutProps {
  children: React.ReactNode;
}

export default function BlogLayout({ children }: BlogLayoutProps) {
  return (
    <div className="blog-layout">
      <aside>
        <h2>Blog Sidebar</h2>
        <ul>
          <li>
            <a href="/blog/react">React Posts</a>
          </li>
          <li>
            <a href="/blog/nextjs">Next.js Posts</a>
          </li>
        </ul>
      </aside>
      <div className="blog-content">{children}</div>
    </div>
  );
}

// app/blog/[slug]/page.tsx - Dynamic Route
interface BlogPostPageProps {
  params: { slug: string };
}

export default async function BlogPostPage({ params }: BlogPostPageProps) {
  // This runs on the server
  const post = await fetch(`https://api.example.com/posts/${params.slug}`).then(
    (res) => res.json()
  );

  return (
    <article>
      <h1>{post.title}</h1>
      <div>{post.content}</div>
    </article>
  );
}

// app/blog/[slug]/loading.tsx - Loading UI
export default function Loading() {
  return (
    <div>
      <h1>Loading blog post...</h1>
      <div className="skeleton" />
    </div>
  );
}

// app/blog/[slug]/error.tsx - Error UI
("use client");

interface ErrorPageProps {
  error: Error;
  reset: () => void;
}

export default function Error({ error, reset }: ErrorPageProps) {
  return (
    <div>
      <h2>Something went wrong!</h2>
      <p>{error.message}</p>
      <button onClick={reset}>Try again</button>
    </div>
  );
}
```

**Directory Structure:**

```
app/
├── layout.tsx           // Root layout
├── page.tsx            // Home page
├── loading.tsx         // Global loading
├── error.tsx           // Global error
├── globals.css         // Global styles
├── blog/
│   ├── layout.tsx      // Blog layout
│   ├── page.tsx        // Blog listing
│   ├── [slug]/
│   │   ├── page.tsx    // Individual blog post
│   │   ├── loading.tsx // Post loading
│   │   └── error.tsx   // Post error
│   └── create/
│       └── page.tsx    // Create post
└── api/
    └── posts/
        └── route.ts    // API endpoint
```

</details>

---

## Performance Optimization & TypeScript

<details>
<summary>
    <h3>84. Advanced Performance Optimization: When and how to use React.memo, useMemo, and useCallback?</h3>
</summary>

Understanding when and how to use these optimization techniques is crucial for building performant React applications.

**React.memo - Component Memoization:**

```tsx
// TypeScript interface for props
interface UserCardProps {
  user: {
    id: number;
    name: string;
    email: string;
  };
  onEdit: (userId: number) => void;
}

// Memoized component - only re-renders when props change
const UserCard = React.memo(({ user, onEdit }: UserCardProps) => {
  console.log("UserCard rendered for:", user.name);

  return (
    <div className="user-card">
      <h3>{user.name}</h3>
      <p>{user.email}</p>
      <button onClick={() => onEdit(user.id)}>Edit</button>
    </div>
  );
});

// Custom comparison function for React.memo
const UserCardWithCustomComparison = React.memo(
  ({ user, onEdit }: UserCardProps) => {
    return (
      <div className="user-card">
        <h3>{user.name}</h3>
        <p>{user.email}</p>
        <button onClick={() => onEdit(user.id)}>Edit</button>
      </div>
    );
  },
  (prevProps, nextProps) => {
    // Only re-render if user data actually changed
    return (
      prevProps.user.id === nextProps.user.id &&
      prevProps.user.name === nextProps.user.name &&
      prevProps.user.email === nextProps.user.email
    );
  }
);
```

**useMemo - Value Memoization:**

```tsx
interface Product {
  id: number;
  name: string;
  price: number;
  category: string;
}

interface ProductListProps {
  products: Product[];
  filter: string;
  sortBy: "name" | "price";
}

function ProductList({ products, filter, sortBy }: ProductListProps) {
  // Expensive computation - only runs when dependencies change
  const filteredAndSortedProducts = useMemo(() => {
    console.log("Computing filtered and sorted products");

    return products
      .filter(
        (product) =>
          product.name.toLowerCase().includes(filter.toLowerCase()) ||
          product.category.toLowerCase().includes(filter.toLowerCase())
      )
      .sort((a, b) => {
        if (sortBy === "name") {
          return a.name.localeCompare(b.name);
        }
        return a.price - b.price;
      });
  }, [products, filter, sortBy]);

  // Memoized calculation
  const totalValue = useMemo(() => {
    return filteredAndSortedProducts.reduce(
      (sum, product) => sum + product.price,
      0
    );
  }, [filteredAndSortedProducts]);

  return (
    <div>
      <h2>Products (Total: ${totalValue.toFixed(2)})</h2>
      {filteredAndSortedProducts.map((product) => (
        <div key={product.id}>
          <h3>{product.name}</h3>
          <p>${product.price}</p>
        </div>
      ))}
    </div>
  );
}
```

**useCallback - Function Memoization:**

```tsx
interface TodoListProps {
  todos: Array<{
    id: number;
    text: string;
    completed: boolean;
  }>;
}

function TodoList({ todos }: TodoListProps) {
  const [filter, setFilter] = useState<"all" | "active" | "completed">("all");

  // Memoized callback - prevents child re-renders
  const handleToggleTodo = useCallback((todoId: number) => {
    setTodos((prevTodos) =>
      prevTodos.map((todo) =>
        todo.id === todoId ? { ...todo, completed: !todo.completed } : todo
      )
    );
  }, []); // Empty dependency array since setTodos is stable

  // Memoized callback with dependencies
  const handleFilterChange = useCallback(
    (newFilter: "all" | "active" | "completed") => {
      console.log("Filter changed to:", newFilter);
      setFilter(newFilter);
    },
    []
  );

  // Memoized filtered todos
  const filteredTodos = useMemo(() => {
    switch (filter) {
      case "active":
        return todos.filter((todo) => !todo.completed);
      case "completed":
        return todos.filter((todo) => todo.completed);
      default:
        return todos;
    }
  }, [todos, filter]);

  return (
    <div>
      <FilterButtons
        currentFilter={filter}
        onFilterChange={handleFilterChange}
      />
      {filteredTodos.map((todo) => (
        <TodoItem key={todo.id} todo={todo} onToggle={handleToggleTodo} />
      ))}
    </div>
  );
}

// Child component that benefits from memoized props
const TodoItem = React.memo(
  ({
    todo,
    onToggle,
  }: {
    todo: { id: number; text: string; completed: boolean };
    onToggle: (id: number) => void;
  }) => {
    console.log("TodoItem rendered:", todo.text);

    return (
      <div>
        <input
          type="checkbox"
          checked={todo.completed}
          onChange={() => onToggle(todo.id)}
        />
        <span
          style={{ textDecoration: todo.completed ? "line-through" : "none" }}
        >
          {todo.text}
        </span>
      </div>
    );
  }
);
```

**When to use each:**

- **React.memo**: When component re-renders frequently with same props
- **useMemo**: For expensive calculations or object creation
- **useCallback**: For functions passed as props to memoized components

**Anti-patterns to avoid:**

```tsx
// ❌ Don't memoize everything
const OverOptimized = React.memo(() => {
  const simpleValue = useMemo(() => 1 + 1, []); // Unnecessary
  const simpleCallback = useCallback(() => {
    console.log("hello");
  }, []); // May not be worth it

  return <div>{simpleValue}</div>;
});

// ✅ Only optimize when there's a performance issue
const WellOptimized = () => {
  const expensiveValue = useMemo(() => {
    return heavyComputation(largeDataSet);
  }, [largeDataSet]);

  return <div>{expensiveValue}</div>;
};
```

</details>

<details>
<summary>
    <h3>85. TypeScript with React: Advanced Patterns and Best Practices</h3>
</summary>

Here are advanced TypeScript patterns for React development with proper type safety and reusability.

**Generic Components:**

```tsx
// Generic List Component
interface ListItem {
  id: string | number;
}

interface ListProps<T extends ListItem> {
  items: T[];
  renderItem: (item: T) => React.ReactNode;
  keyExtractor?: (item: T) => string | number;
  emptyMessage?: string;
}

function List<T extends ListItem>({
  items,
  renderItem,
  keyExtractor = (item) => item.id,
  emptyMessage = "No items found",
}: ListProps<T>) {
  if (items.length === 0) {
    return <div className="empty-state">{emptyMessage}</div>;
  }

  return (
    <div className="list">
      {items.map((item) => (
        <div key={keyExtractor(item)} className="list-item">
          {renderItem(item)}
        </div>
      ))}
    </div>
  );
}

// Usage with different data types
interface User {
  id: number;
  name: string;
  email: string;
}

interface Product {
  id: string;
  title: string;
  price: number;
}

function App() {
  const users: User[] = [{ id: 1, name: "John", email: "john@example.com" }];

  const products: Product[] = [{ id: "prod-1", title: "Laptop", price: 999 }];

  return (
    <div>
      <List
        items={users}
        renderItem={(user) => (
          <div>
            <h3>{user.name}</h3>
            <p>{user.email}</p>
          </div>
        )}
      />

      <List
        items={products}
        renderItem={(product) => (
          <div>
            <h3>{product.title}</h3>
            <p>${product.price}</p>
          </div>
        )}
        keyExtractor={(product) => product.id}
      />
    </div>
  );
}
```

**Advanced Hook Types:**

```tsx
// Custom hook with proper TypeScript
interface UseApiResult<T> {
  data: T | null;
  loading: boolean;
  error: string | null;
  refetch: () => Promise<void>;
}

function useApi<T>(url: string, options?: RequestInit): UseApiResult<T> {
  const [data, setData] = useState<T | null>(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState<string | null>(null);

  const fetchData = useCallback(async () => {
    try {
      setLoading(true);
      setError(null);

      const response = await fetch(url, options);

      if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
      }

      const result = await response.json();
      setData(result);
    } catch (err) {
      setError(err instanceof Error ? err.message : "An error occurred");
    } finally {
      setLoading(false);
    }
  }, [url, options]);

  useEffect(() => {
    fetchData();
  }, [fetchData]);

  return { data, loading, error, refetch: fetchData };
}

// Usage with typed responses
interface ApiUser {
  id: number;
  name: string;
  email: string;
  avatar?: string;
}

function UserProfile({ userId }: { userId: number }) {
  const {
    data: user,
    loading,
    error,
    refetch,
  } = useApi<ApiUser>(`/api/users/${userId}`);

  if (loading) return <div>Loading user...</div>;
  if (error) return <div>Error: {error}</div>;
  if (!user) return <div>User not found</div>;

  return (
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
      {user.avatar && <img src={user.avatar} alt={user.name} />}
      <button onClick={refetch}>Refresh</button>
    </div>
  );
}
```

**Form Handling with TypeScript:**

```tsx
// Type-safe form handling
interface FormData {
  email: string;
  password: string;
  rememberMe: boolean;
}

type FormErrors = Partial<Record<keyof FormData, string>>;

interface UseFormResult<T> {
  values: T;
  errors: Partial<Record<keyof T, string>>;
  handleChange: (
    field: keyof T
  ) => (event: React.ChangeEvent<HTMLInputElement>) => void;
  handleSubmit: (
    onSubmit: (values: T) => void
  ) => (event: React.FormEvent) => void;
  setFieldError: (field: keyof T, error: string) => void;
  clearErrors: () => void;
}

function useForm<T extends Record<string, any>>(
  initialValues: T,
  validator?: (values: T) => Partial<Record<keyof T, string>>
): UseFormResult<T> {
  const [values, setValues] = useState<T>(initialValues);
  const [errors, setErrors] = useState<Partial<Record<keyof T, string>>>({});

  const handleChange = useCallback(
    (field: keyof T) => (event: React.ChangeEvent<HTMLInputElement>) => {
      const { value, type, checked } = event.target;
      setValues((prev) => ({
        ...prev,
        [field]: type === "checkbox" ? checked : value,
      }));

      // Clear error when user starts typing
      if (errors[field]) {
        setErrors((prev) => ({ ...prev, [field]: undefined }));
      }
    },
    [errors]
  );

  const setFieldError = useCallback((field: keyof T, error: string) => {
    setErrors((prev) => ({ ...prev, [field]: error }));
  }, []);

  const clearErrors = useCallback(() => {
    setErrors({});
  }, []);

  const handleSubmit = useCallback(
    (onSubmit: (values: T) => void) => (event: React.FormEvent) => {
      event.preventDefault();

      const validationErrors = validator?.(values) || {};

      if (Object.keys(validationErrors).length > 0) {
        setErrors(validationErrors);
        return;
      }

      onSubmit(values);
    },
    [values, validator]
  );

  return {
    values,
    errors,
    handleChange,
    handleSubmit,
    setFieldError,
    clearErrors,
  };
}

// Login form implementation
function LoginForm() {
  const validateForm = (values: FormData): FormErrors => {
    const errors: FormErrors = {};

    if (!values.email) {
      errors.email = "Email is required";
    } else if (!/\S+@\S+\.\S+/.test(values.email)) {
      errors.email = "Email is invalid";
    }

    if (!values.password) {
      errors.password = "Password is required";
    } else if (values.password.length < 6) {
      errors.password = "Password must be at least 6 characters";
    }

    return errors;
  };

  const { values, errors, handleChange, handleSubmit, setFieldError } =
    useForm<FormData>(
      { email: "", password: "", rememberMe: false },
      validateForm
    );

  const onSubmit = async (formData: FormData) => {
    try {
      const response = await fetch("/api/login", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(formData),
      });

      if (!response.ok) {
        setFieldError("email", "Invalid credentials");
        return;
      }

      console.log("Login successful!");
    } catch (error) {
      setFieldError("email", "Network error occurred");
    }
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <div>
        <label htmlFor="email">Email:</label>
        <input
          id="email"
          type="email"
          value={values.email}
          onChange={handleChange("email")}
        />
        {errors.email && <span className="error">{errors.email}</span>}
      </div>

      <div>
        <label htmlFor="password">Password:</label>
        <input
          id="password"
          type="password"
          value={values.password}
          onChange={handleChange("password")}
        />
        {errors.password && <span className="error">{errors.password}</span>}
      </div>

      <div>
        <label>
          <input
            type="checkbox"
            checked={values.rememberMe}
            onChange={handleChange("rememberMe")}
          />
          Remember me
        </label>
      </div>

      <button type="submit">Login</button>
    </form>
  );
}
```

**Component Props with Variants:**

```tsx
// Button component with variants
type ButtonVariant = "primary" | "secondary" | "danger" | "outline";
type ButtonSize = "sm" | "md" | "lg";

interface BaseButtonProps {
  variant?: ButtonVariant;
  size?: ButtonSize;
  loading?: boolean;
  disabled?: boolean;
  children: React.ReactNode;
}

type ButtonProps = BaseButtonProps &
  React.ButtonHTMLAttributes<HTMLButtonElement>;

const Button = React.forwardRef<HTMLButtonElement, ButtonProps>(
  (
    {
      variant = "primary",
      size = "md",
      loading = false,
      disabled = false,
      children,
      className = "",
      ...rest
    },
    ref
  ) => {
    const baseClasses = "btn";
    const variantClasses = `btn--${variant}`;
    const sizeClasses = `btn--${size}`;
    const loadingClasses = loading ? "btn--loading" : "";

    const buttonClasses = [
      baseClasses,
      variantClasses,
      sizeClasses,
      loadingClasses,
      className,
    ]
      .filter(Boolean)
      .join(" ");

    return (
      <button
        ref={ref}
        className={buttonClasses}
        disabled={disabled || loading}
        {...rest}
      >
        {loading ? <span>Loading...</span> : children}
      </button>
    );
  }
);

Button.displayName = "Button";

// Usage
function App() {
  return (
    <div>
      <Button
        variant="primary"
        size="lg"
        onClick={() => console.log("Primary clicked")}
      >
        Primary Button
      </Button>

      <Button variant="danger" loading>
        Deleting...
      </Button>

      <Button variant="outline" disabled>
        Disabled Button
      </Button>
    </div>
  );
}
```

</details>

---

## React Testing & Best Practices

<details>
<summary>
    <h3>86. How do you test React components with React Testing Library and TypeScript?</h3>
</summary>

React Testing Library with TypeScript provides excellent tools for testing React components in a way that resembles how users interact with your application.

**Basic Component Testing:**

```tsx
// UserCard.tsx
interface User {
  id: number;
  name: string;
  email: string;
  isActive: boolean;
}

interface UserCardProps {
  user: User;
  onEdit: (userId: number) => void;
  onDelete: (userId: number) => void;
}

export function UserCard({ user, onEdit, onDelete }: UserCardProps) {
  return (
    <div data-testid={`user-card-${user.id}`}>
      <h3>{user.name}</h3>
      <p>{user.email}</p>
      <span className={user.isActive ? "active" : "inactive"}>
        {user.isActive ? "Active" : "Inactive"}
      </span>
      <button onClick={() => onEdit(user.id)}>Edit</button>
      <button onClick={() => onDelete(user.id)}>Delete</button>
    </div>
  );
}

// UserCard.test.tsx
import { render, screen, fireEvent } from "@testing-library/react";
import { UserCard } from "./UserCard";

const mockUser: User = {
  id: 1,
  name: "John Doe",
  email: "john@example.com",
  isActive: true,
};

describe("UserCard", () => {
  const mockOnEdit = jest.fn();
  const mockOnDelete = jest.fn();

  beforeEach(() => {
    mockOnEdit.mockClear();
    mockOnDelete.mockClear();
  });

  it("renders user information correctly", () => {
    render(
      <UserCard user={mockUser} onEdit={mockOnEdit} onDelete={mockOnDelete} />
    );

    expect(screen.getByText("John Doe")).toBeInTheDocument();
    expect(screen.getByText("john@example.com")).toBeInTheDocument();
    expect(screen.getByText("Active")).toBeInTheDocument();
  });

  it("calls onEdit when edit button is clicked", () => {
    render(
      <UserCard user={mockUser} onEdit={mockOnEdit} onDelete={mockOnDelete} />
    );

    fireEvent.click(screen.getByText("Edit"));
    expect(mockOnEdit).toHaveBeenCalledWith(1);
    expect(mockOnEdit).toHaveBeenCalledTimes(1);
  });

  it("calls onDelete when delete button is clicked", () => {
    render(
      <UserCard user={mockUser} onEdit={mockOnEdit} onDelete={mockOnDelete} />
    );

    fireEvent.click(screen.getByText("Delete"));
    expect(mockOnDelete).toHaveBeenCalledWith(1);
  });

  it("displays correct status for inactive user", () => {
    const inactiveUser = { ...mockUser, isActive: false };

    render(
      <UserCard
        user={inactiveUser}
        onEdit={mockOnEdit}
        onDelete={mockOnDelete}
      />
    );

    expect(screen.getByText("Inactive")).toBeInTheDocument();
    expect(screen.getByText("Inactive")).toHaveClass("inactive");
  });
});
```

**Testing Custom Hooks:**

```tsx
// useCounter.ts
import { useState, useCallback } from "react";

interface UseCounterResult {
  count: number;
  increment: () => void;
  decrement: () => void;
  reset: () => void;
  setCount: (value: number) => void;
}

export function useCounter(initialValue: number = 0): UseCounterResult {
  const [count, setCount] = useState(initialValue);

  const increment = useCallback(() => {
    setCount((prev) => prev + 1);
  }, []);

  const decrement = useCallback(() => {
    setCount((prev) => prev - 1);
  }, []);

  const reset = useCallback(() => {
    setCount(initialValue);
  }, [initialValue]);

  return {
    count,
    increment,
    decrement,
    reset,
    setCount,
  };
}

// useCounter.test.ts
import { renderHook, act } from "@testing-library/react";
import { useCounter } from "./useCounter";

describe("useCounter", () => {
  it("initializes with default value", () => {
    const { result } = renderHook(() => useCounter());
    expect(result.current.count).toBe(0);
  });

  it("initializes with custom value", () => {
    const { result } = renderHook(() => useCounter(10));
    expect(result.current.count).toBe(10);
  });

  it("increments count", () => {
    const { result } = renderHook(() => useCounter(5));

    act(() => {
      result.current.increment();
    });

    expect(result.current.count).toBe(6);
  });

  it("decrements count", () => {
    const { result } = renderHook(() => useCounter(5));

    act(() => {
      result.current.decrement();
    });

    expect(result.current.count).toBe(4);
  });

  it("resets to initial value", () => {
    const { result } = renderHook(() => useCounter(10));

    act(() => {
      result.current.increment();
      result.current.increment();
    });

    expect(result.current.count).toBe(12);

    act(() => {
      result.current.reset();
    });

    expect(result.current.count).toBe(10);
  });

  it("sets count to specific value", () => {
    const { result } = renderHook(() => useCounter());

    act(() => {
      result.current.setCount(25);
    });

    expect(result.current.count).toBe(25);
  });
});
```

**Testing Components with Context:**

```tsx
// AuthContext.tsx
interface User {
  id: string;
  name: string;
  role: "admin" | "user";
}

interface AuthContextType {
  user: User | null;
  login: (user: User) => void;
  logout: () => void;
  isAdmin: boolean;
}

const AuthContext = createContext<AuthContextType | null>(null);

export function AuthProvider({ children }: { children: React.ReactNode }) {
  const [user, setUser] = useState<User | null>(null);

  const login = useCallback((user: User) => {
    setUser(user);
  }, []);

  const logout = useCallback(() => {
    setUser(null);
  }, []);

  const isAdmin = user?.role === "admin";

  return (
    <AuthContext.Provider value={{ user, login, logout, isAdmin }}>
      {children}
    </AuthContext.Provider>
  );
}

export function useAuth() {
  const context = useContext(AuthContext);
  if (!context) {
    throw new Error("useAuth must be used within AuthProvider");
  }
  return context;
}

// AdminPanel.tsx
export function AdminPanel() {
  const { user, isAdmin, logout } = useAuth();

  if (!isAdmin) {
    return <div>Access denied. Admin rights required.</div>;
  }

  return (
    <div>
      <h1>Admin Panel</h1>
      <p>Welcome, {user?.name}</p>
      <button onClick={logout}>Logout</button>
    </div>
  );
}

// AdminPanel.test.tsx
import { render, screen, fireEvent } from "@testing-library/react";
import { AuthProvider } from "./AuthContext";
import { AdminPanel } from "./AdminPanel";

const renderWithAuth = (ui: React.ReactElement, { user = null } = {}) => {
  function Wrapper({ children }: { children: React.ReactNode }) {
    return <AuthProvider>{children}</AuthProvider>;
  }

  const result = render(ui, { wrapper: Wrapper });

  // If user is provided, log them in
  if (user) {
    const authContext = result.container.querySelector(
      '[data-testid="auth-provider"]'
    );
    // In real implementation, you'd expose the login function through a test helper
  }

  return result;
};

// Custom render helper with authenticated user
const renderWithAuthenticatedUser = (ui: React.ReactElement, user: User) => {
  function AuthWrapper({ children }: { children: React.ReactNode }) {
    return (
      <AuthProvider>
        <div data-testid="auth-wrapper">{children}</div>
      </AuthProvider>
    );
  }

  const result = render(ui, { wrapper: AuthWrapper });

  // You would typically expose a way to set the user in tests
  // This is a simplified example
  return result;
};

describe("AdminPanel", () => {
  const adminUser: User = {
    id: "1",
    name: "Admin User",
    role: "admin",
  };

  const regularUser: User = {
    id: "2",
    name: "Regular User",
    role: "user",
  };

  it("denies access for non-admin users", () => {
    // This test would need proper setup with the context
    render(
      <AuthProvider>
        <AdminPanel />
      </AuthProvider>
    );

    expect(
      screen.getByText("Access denied. Admin rights required.")
    ).toBeInTheDocument();
  });

  it("shows admin panel for admin users", () => {
    // You would set up the authenticated admin user here
    // This is a simplified test structure
  });
});
```

**Testing Async Components:**

```tsx
// UserList.tsx
interface User {
  id: number;
  name: string;
  email: string;
}

export function UserList() {
  const [users, setUsers] = useState<User[]>([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState<string | null>(null);

  useEffect(() => {
    const fetchUsers = async () => {
      try {
        const response = await fetch("/api/users");
        if (!response.ok) {
          throw new Error("Failed to fetch users");
        }
        const userData = await response.json();
        setUsers(userData);
      } catch (err) {
        setError(err instanceof Error ? err.message : "Unknown error");
      } finally {
        setLoading(false);
      }
    };

    fetchUsers();
  }, []);

  if (loading) return <div>Loading users...</div>;
  if (error) return <div>Error: {error}</div>;

  return (
    <div>
      <h1>Users</h1>
      {users.map((user) => (
        <div key={user.id} data-testid={`user-${user.id}`}>
          <h3>{user.name}</h3>
          <p>{user.email}</p>
        </div>
      ))}
    </div>
  );
}

// UserList.test.tsx
import { render, screen, waitFor } from "@testing-library/react";
import { UserList } from "./UserList";

// Mock fetch
global.fetch = jest.fn();
const mockFetch = fetch as jest.MockedFunction<typeof fetch>;

const mockUsers: User[] = [
  { id: 1, name: "John Doe", email: "john@example.com" },
  { id: 2, name: "Jane Smith", email: "jane@example.com" },
];

describe("UserList", () => {
  beforeEach(() => {
    mockFetch.mockClear();
  });

  it("displays loading state initially", () => {
    mockFetch.mockReturnValue(
      Promise.resolve({
        ok: true,
        json: () => Promise.resolve(mockUsers),
      } as Response)
    );

    render(<UserList />);
    expect(screen.getByText("Loading users...")).toBeInTheDocument();
  });

  it("displays users after successful fetch", async () => {
    mockFetch.mockResolvedValue({
      ok: true,
      json: () => Promise.resolve(mockUsers),
    } as Response);

    render(<UserList />);

    await waitFor(() => {
      expect(screen.getByText("Users")).toBeInTheDocument();
    });

    expect(screen.getByText("John Doe")).toBeInTheDocument();
    expect(screen.getByText("jane@example.com")).toBeInTheDocument();
  });

  it("displays error message on fetch failure", async () => {
    mockFetch.mockRejectedValue(new Error("Network error"));

    render(<UserList />);

    await waitFor(() => {
      expect(screen.getByText(/Error: Network error/)).toBeInTheDocument();
    });
  });

  it("handles HTTP error responses", async () => {
    mockFetch.mockResolvedValue({
      ok: false,
      status: 404,
    } as Response);

    render(<UserList />);

    await waitFor(() => {
      expect(
        screen.getByText(/Error: Failed to fetch users/)
      ).toBeInTheDocument();
    });
  });
});
```

**Test Setup Configuration:**

```typescript
// setupTests.ts
import "@testing-library/jest-dom";
import { configure } from "@testing-library/react";

// Configure testing library
configure({ testIdAttribute: "data-testid" });

// Mock IntersectionObserver
global.IntersectionObserver = class IntersectionObserver {
  constructor() {}
  disconnect() {}
  observe() {}
  unobserve() {}
};

// Mock ResizeObserver
global.ResizeObserver = class ResizeObserver {
  constructor(cb: any) {}
  observe() {}
  unobserve() {}
  disconnect() {}
};
```

</details>

---

## React Security & Accessibility

<details>
<summary>
    <h3>87. What are the common security vulnerabilities in React applications and how to prevent them?</h3>
</summary>

React applications can be vulnerable to several security threats. Here are the most common ones and how to prevent them:

**1. Cross-Site Scripting (XSS):**

```tsx
// ❌ Dangerous - allows XSS attacks
interface UnsafeComponentProps {
  userContent: string;
}

function UnsafeComponent({ userContent }: UnsafeComponentProps) {
  // This directly injects HTML and can execute malicious scripts
  return <div dangerouslySetInnerHTML={{ __html: userContent }} />;
}

// ✅ Safe approaches
import DOMPurify from "dompurify";

function SafeComponent({ userContent }: UnsafeComponentProps) {
  // Approach 1: Use React's built-in XSS protection
  return <div>{userContent}</div>; // React automatically escapes content

  // Approach 2: Sanitize HTML content
  const sanitizedContent = DOMPurify.sanitize(userContent);
  return <div dangerouslySetInnerHTML={{ __html: sanitizedContent }} />;
}

// Safe handling of user input
function CommentComponent({ comment }: { comment: string }) {
  // React automatically escapes this content
  return (
    <div className="comment">
      <p>{comment}</p> {/* Safe - React escapes special characters */}
    </div>
  );
}
```

**2. Dependency Vulnerabilities:**

```bash
# Regular security audits
npm audit
npm audit fix

# Use tools like Snyk
npx snyk test
npx snyk monitor

# Keep dependencies updated
npm update
npm outdated
```

**3. Environment Variables Security:**

```typescript
// ❌ Don't expose sensitive data in client-side code
const API_KEY = process.env.REACT_APP_SECRET_API_KEY; // Exposed to client!

// ✅ Safe approach
// Only expose non-sensitive public variables
const PUBLIC_API_URL = process.env.REACT_APP_PUBLIC_API_URL;

// Keep sensitive data on the server
// server-side API call
async function getSecureData() {
  const response = await fetch("/api/secure-endpoint", {
    headers: {
      Authorization: `Bearer ${await getAuthToken()}`, // Server-side token
    },
  });
  return response.json();
}
```

**4. Authentication & Authorization:**

```tsx
// Secure authentication implementation
interface AuthToken {
  token: string;
  expiresAt: number;
  refreshToken: string;
}

class AuthService {
  private static readonly TOKEN_KEY = "auth_token";
  private static readonly REFRESH_KEY = "refresh_token";

  static setTokens(tokens: AuthToken): void {
    // Store tokens securely (consider httpOnly cookies for production)
    localStorage.setItem(this.TOKEN_KEY, tokens.token);
    localStorage.setItem(this.REFRESH_KEY, tokens.refreshToken);
  }

  static getToken(): string | null {
    const token = localStorage.getItem(this.TOKEN_KEY);
    if (token && this.isTokenValid(token)) {
      return token;
    }
    return null;
  }

  static isTokenValid(token: string): boolean {
    try {
      const payload = JSON.parse(atob(token.split(".")[1]));
      return payload.exp * 1000 > Date.now();
    } catch {
      return false;
    }
  }

  static async refreshToken(): Promise<string | null> {
    const refreshToken = localStorage.getItem(this.REFRESH_KEY);
    if (!refreshToken) return null;

    try {
      const response = await fetch("/api/auth/refresh", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ refreshToken }),
      });

      if (response.ok) {
        const newTokens = await response.json();
        this.setTokens(newTokens);
        return newTokens.token;
      }
    } catch (error) {
      console.error("Token refresh failed:", error);
    }

    return null;
  }

  static clearTokens(): void {
    localStorage.removeItem(this.TOKEN_KEY);
    localStorage.removeItem(this.REFRESH_KEY);
  }
}

// Protected Route Component
function ProtectedRoute({
  children,
  requiredRole,
}: {
  children: React.ReactNode;
  requiredRole?: string;
}) {
  const { user, isAuthenticated } = useAuth();

  if (!isAuthenticated) {
    return <Navigate to="/login" replace />;
  }

  if (requiredRole && user?.role !== requiredRole) {
    return <Navigate to="/unauthorized" replace />;
  }

  return <>{children}</>;
}
```

**5. CSRF Protection:**

```tsx
// CSRF token handling
function CSRFProtectedForm() {
  const [csrfToken, setCsrfToken] = useState<string>("");

  useEffect(() => {
    // Get CSRF token from meta tag or API
    const token = document
      .querySelector('meta[name="csrf-token"]')
      ?.getAttribute("content");
    setCsrfToken(token || "");
  }, []);

  const handleSubmit = async (formData: any) => {
    await fetch("/api/protected-endpoint", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "X-CSRF-Token": csrfToken, // Include CSRF token
        Authorization: `Bearer ${AuthService.getToken()}`,
      },
      body: JSON.stringify(formData),
    });
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* Form content */}
      <input type="hidden" name="_token" value={csrfToken} />
    </form>
  );
}
```

**6. Content Security Policy (CSP):**

```html
<!-- Add to index.html -->
<meta
  http-equiv="Content-Security-Policy"
  content="default-src 'self'; 
               script-src 'self' 'unsafe-inline' https://trusted-cdn.com; 
               style-src 'self' 'unsafe-inline'; 
               img-src 'self' data: https:; 
               connect-src 'self' https://api.yourapp.com;"
/>
```

**7. Input Validation:**

```tsx
// Comprehensive input validation
interface FormValidation {
  email: (value: string) => string | null;
  password: (value: string) => string | null;
  url: (value: string) => string | null;
}

const validation: FormValidation = {
  email: (value: string) => {
    if (!value) return "Email is required";
    if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(value)) {
      return "Please enter a valid email address";
    }
    if (value.length > 254) return "Email is too long";
    return null;
  },

  password: (value: string) => {
    if (!value) return "Password is required";
    if (value.length < 8) return "Password must be at least 8 characters";
    if (!/(?=.*[a-z])(?=.*[A-Z])(?=.*\d)/.test(value)) {
      return "Password must contain uppercase, lowercase, and number";
    }
    return null;
  },

  url: (value: string) => {
    if (!value) return null; // Optional field
    try {
      const url = new URL(value);
      if (!["http:", "https:"].includes(url.protocol)) {
        return "URL must use HTTP or HTTPS protocol";
      }
      return null;
    } catch {
      return "Please enter a valid URL";
    }
  },
};

// Secure form component
function SecureForm() {
  const [formData, setFormData] = useState({
    email: "",
    password: "",
    website: "",
  });
  const [errors, setErrors] = useState<Record<string, string>>({});

  const validateField = (name: string, value: string) => {
    const validator = validation[name as keyof FormValidation];
    return validator ? validator(value) : null;
  };

  const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    const { name, value } = e.target;

    // Sanitize input
    const sanitizedValue = value.trim().slice(0, 1000); // Limit length

    setFormData((prev) => ({ ...prev, [name]: sanitizedValue }));

    // Real-time validation
    const error = validateField(name, sanitizedValue);
    setErrors((prev) => ({ ...prev, [name]: error || "" }));
  };

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();

    // Validate all fields
    const newErrors: Record<string, string> = {};
    Object.entries(formData).forEach(([key, value]) => {
      const error = validateField(key, value);
      if (error) newErrors[key] = error;
    });

    if (Object.keys(newErrors).length > 0) {
      setErrors(newErrors);
      return;
    }

    // Submit data securely
    await submitForm(formData);
  };

  return (
    <form onSubmit={handleSubmit} noValidate>
      <div>
        <input
          type="email"
          name="email"
          value={formData.email}
          onChange={handleChange}
          autoComplete="email"
          required
          aria-invalid={!!errors.email}
          aria-describedby={errors.email ? "email-error" : undefined}
        />
        {errors.email && (
          <div id="email-error" role="alert">
            {errors.email}
          </div>
        )}
      </div>

      <div>
        <input
          type="password"
          name="password"
          value={formData.password}
          onChange={handleChange}
          autoComplete="current-password"
          required
          aria-invalid={!!errors.password}
        />
        {errors.password && <div role="alert">{errors.password}</div>}
      </div>

      <button type="submit">Submit</button>
    </form>
  );
}
```

</details>

<details>
<summary>
    <h3>88. How do you implement accessibility (a11y) in React applications?</h3>
</summary>

Accessibility is crucial for making React applications usable by everyone. Here are key techniques and patterns:

**1. Semantic HTML and ARIA:**

```tsx
// Good semantic structure
interface NavigationProps {
  items: Array<{ href: string; label: string; current?: boolean }>;
}

function AccessibleNavigation({ items }: NavigationProps) {
  return (
    <nav aria-label="Main navigation">
      <ul role="list">
        {items.map((item, index) => (
          <li key={item.href}>
            <a
              href={item.href}
              aria-current={item.current ? "page" : undefined}
              className={item.current ? "current-page" : ""}
            >
              {item.label}
            </a>
          </li>
        ))}
      </ul>
    </nav>
  );
}

// Modal with proper ARIA
interface ModalProps {
  isOpen: boolean;
  onClose: () => void;
  title: string;
  children: React.ReactNode;
}

function AccessibleModal({ isOpen, onClose, title, children }: ModalProps) {
  const modalRef = useRef<HTMLDivElement>(null);
  const previousFocusRef = useRef<HTMLElement | null>(null);

  useEffect(() => {
    if (isOpen) {
      // Store current focus
      previousFocusRef.current = document.activeElement as HTMLElement;

      // Focus modal
      modalRef.current?.focus();

      // Trap focus within modal
      const trapFocus = (e: KeyboardEvent) => {
        if (e.key === "Escape") {
          onClose();
        }
      };

      document.addEventListener("keydown", trapFocus);
      return () => document.removeEventListener("keydown", trapFocus);
    } else {
      // Return focus to previous element
      previousFocusRef.current?.focus();
    }
  }, [isOpen, onClose]);

  if (!isOpen) return null;

  return (
    <div
      className="modal-backdrop"
      onClick={(e) => e.target === e.currentTarget && onClose()}
    >
      <div
        ref={modalRef}
        className="modal"
        role="dialog"
        aria-modal="true"
        aria-labelledby="modal-title"
        tabIndex={-1}
      >
        <div className="modal-header">
          <h2 id="modal-title">{title}</h2>
          <button
            onClick={onClose}
            aria-label="Close modal"
            className="close-button"
          >
            ×
          </button>
        </div>
        <div className="modal-content">{children}</div>
      </div>
    </div>
  );
}
```

**2. Form Accessibility:**

```tsx
// Comprehensive accessible form
interface FormField {
  id: string;
  label: string;
  type: "text" | "email" | "password" | "tel";
  required?: boolean;
  placeholder?: string;
  autoComplete?: string;
}

interface AccessibleFormProps {
  fields: FormField[];
  onSubmit: (data: Record<string, string>) => void;
}

function AccessibleForm({ fields, onSubmit }: AccessibleFormProps) {
  const [formData, setFormData] = useState<Record<string, string>>({});
  const [errors, setErrors] = useState<Record<string, string>>({});
  const [isSubmitting, setIsSubmitting] = useState(false);

  const firstErrorRef = useRef<HTMLInputElement>(null);

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    setIsSubmitting(true);

    // Validate form
    const newErrors: Record<string, string> = {};
    fields.forEach((field) => {
      if (field.required && !formData[field.id]) {
        newErrors[field.id] = `${field.label} is required`;
      }
    });

    if (Object.keys(newErrors).length > 0) {
      setErrors(newErrors);
      // Focus first error field
      setTimeout(() => firstErrorRef.current?.focus(), 0);
      setIsSubmitting(false);
      return;
    }

    try {
      await onSubmit(formData);
    } catch (error) {
      setErrors({ general: "An error occurred while submitting the form" });
    } finally {
      setIsSubmitting(false);
    }
  };

  const handleChange = (fieldId: string, value: string) => {
    setFormData((prev) => ({ ...prev, [fieldId]: value }));
    // Clear error when user starts typing
    if (errors[fieldId]) {
      setErrors((prev) => ({ ...prev, [fieldId]: "" }));
    }
  };

  return (
    <form onSubmit={handleSubmit} noValidate>
      <fieldset disabled={isSubmitting}>
        <legend>Registration Form</legend>

        {errors.general && (
          <div role="alert" className="error-message">
            {errors.general}
          </div>
        )}

        {fields.map((field, index) => (
          <div key={field.id} className="form-field">
            <label htmlFor={field.id} className="form-label">
              {field.label}
              {field.required && <span aria-label="required"> *</span>}
            </label>

            <input
              ref={
                index === 0 && Object.keys(errors).length > 0
                  ? firstErrorRef
                  : null
              }
              id={field.id}
              type={field.type}
              value={formData[field.id] || ""}
              onChange={(e) => handleChange(field.id, e.target.value)}
              placeholder={field.placeholder}
              autoComplete={field.autoComplete}
              required={field.required}
              aria-invalid={!!errors[field.id]}
              aria-describedby={
                errors[field.id] ? `${field.id}-error` : undefined
              }
              className={errors[field.id] ? "error" : ""}
            />

            {errors[field.id] && (
              <div
                id={`${field.id}-error`}
                role="alert"
                className="field-error"
              >
                {errors[field.id]}
              </div>
            )}
          </div>
        ))}

        <button
          type="submit"
          disabled={isSubmitting}
          aria-describedby={isSubmitting ? "submit-status" : undefined}
        >
          {isSubmitting ? "Submitting..." : "Submit"}
        </button>

        {isSubmitting && (
          <div id="submit-status" aria-live="polite" className="sr-only">
            Form is being submitted
          </div>
        )}
      </fieldset>
    </form>
  );
}
```

**3. Focus Management:**

```tsx
// Custom hook for focus management
function useFocusTrap(isActive: boolean) {
  const containerRef = useRef<HTMLDivElement>(null);

  useEffect(() => {
    if (!isActive) return;

    const container = containerRef.current;
    if (!container) return;

    const focusableElements = container.querySelectorAll(
      'a[href], button, textarea, input[type="text"], input[type="radio"], input[type="checkbox"], select'
    ) as NodeListOf<HTMLElement>;

    const firstElement = focusableElements[0];
    const lastElement = focusableElements[focusableElements.length - 1];

    const handleTabKey = (e: KeyboardEvent) => {
      if (e.key === "Tab") {
        if (e.shiftKey) {
          if (document.activeElement === firstElement) {
            lastElement.focus();
            e.preventDefault();
          }
        } else {
          if (document.activeElement === lastElement) {
            firstElement.focus();
            e.preventDefault();
          }
        }
      }
    };

    document.addEventListener("keydown", handleTabKey);
    firstElement?.focus();

    return () => {
      document.removeEventListener("keydown", handleTabKey);
    };
  }, [isActive]);

  return containerRef;
}

// Skip links for keyboard navigation
function SkipLinks() {
  return (
    <div className="skip-links">
      <a href="#main-content" className="skip-link">
        Skip to main content
      </a>
      <a href="#navigation" className="skip-link">
        Skip to navigation
      </a>
    </div>
  );
}
```

**4. Screen Reader Support:**

```tsx
// Live regions for dynamic content
function useAnnouncement() {
  const [announcement, setAnnouncement] = useState("");

  const announce = useCallback((message: string) => {
    setAnnouncement(message);
    // Clear after announcement
    setTimeout(() => setAnnouncement(""), 1000);
  }, []);

  const AnnouncementRegion = useCallback(
    () => (
      <div
        role="status"
        aria-live="polite"
        aria-atomic="true"
        className="sr-only"
      >
        {announcement}
      </div>
    ),
    [announcement]
  );

  return { announce, AnnouncementRegion };
}

// Data table with proper headers
interface TableData {
  id: string;
  name: string;
  email: string;
  status: "active" | "inactive";
}

interface AccessibleTableProps {
  data: TableData[];
  caption: string;
}

function AccessibleTable({ data, caption }: AccessibleTableProps) {
  const { announce, AnnouncementRegion } = useAnnouncement();

  const handleStatusToggle = (userId: string, currentStatus: string) => {
    const newStatus = currentStatus === "active" ? "inactive" : "active";
    // Update logic here
    announce(`User status changed to ${newStatus}`);
  };

  return (
    <div>
      <table role="table" aria-label={caption}>
        <caption>{caption}</caption>
        <thead>
          <tr>
            <th scope="col" id="name-header">
              Name
            </th>
            <th scope="col" id="email-header">
              Email
            </th>
            <th scope="col" id="status-header">
              Status
            </th>
            <th scope="col" id="actions-header">
              Actions
            </th>
          </tr>
        </thead>
        <tbody>
          {data.map((user) => (
            <tr key={user.id}>
              <td headers="name-header">{user.name}</td>
              <td headers="email-header">{user.email}</td>
              <td headers="status-header">
                <span className={`status status--${user.status}`}>
                  {user.status}
                </span>
              </td>
              <td headers="actions-header">
                <button
                  onClick={() => handleStatusToggle(user.id, user.status)}
                  aria-describedby={`status-description-${user.id}`}
                >
                  Toggle Status
                </button>
                <div id={`status-description-${user.id}`} className="sr-only">
                  Current status: {user.status}. Click to change to{" "}
                  {user.status === "active" ? "inactive" : "active"}
                </div>
              </td>
            </tr>
          ))}
        </tbody>
      </table>
      <AnnouncementRegion />
    </div>
  );
}
```

**5. CSS for Accessibility:**

```css
/* Screen reader only content */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

/* Skip links */
.skip-link {
  position: absolute;
  top: -40px;
  left: 6px;
  background: #000;
  color: #fff;
  padding: 8px;
  text-decoration: none;
  border-radius: 0 0 4px 4px;
  z-index: 1000;
}

.skip-link:focus {
  top: 0;
}

/* Focus styles */
*:focus {
  outline: 2px solid #005fcc;
  outline-offset: 2px;
}

/* High contrast mode support */
@media (prefers-contrast: high) {
  .button {
    border: 2px solid;
  }
}

/* Reduced motion support */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

**6. Testing Accessibility:**

```tsx
// Accessibility testing utilities
import { axe, toHaveNoViolations } from "jest-axe";

expect.extend(toHaveNoViolations);

describe("AccessibleForm", () => {
  it("should have no accessibility violations", async () => {
    const { container } = render(
      <AccessibleForm
        fields={[
          { id: "email", label: "Email", type: "email", required: true },
          {
            id: "password",
            label: "Password",
            type: "password",
            required: true,
          },
        ]}
        onSubmit={jest.fn()}
      />
    );

    const results = await axe(container);
    expect(results).toHaveNoViolations();
  });

  it("should have proper ARIA labels", () => {
    render(
      <AccessibleForm
        fields={[
          { id: "email", label: "Email", type: "email", required: true },
        ]}
        onSubmit={jest.fn()}
      />
    );

    expect(screen.getByLabelText("Email *")).toBeInTheDocument();
    expect(screen.getByRole("textbox", { name: /email/i })).toBeInTheDocument();
  });
});
```

</details>

---

## Advanced React Patterns

<details>
<summary>
    <h3>89. Explain Compound Components pattern and provide a TypeScript example.</h3>
</summary>

Compound Components is a pattern where components work together to form a complete UI. The parent component manages the state and passes it down to child components through context.

```tsx
// Accordion implementation using Compound Components
interface AccordionContextType {
  activeIndex: number | null;
  setActiveIndex: (index: number | null) => void;
}

const AccordionContext = createContext<AccordionContextType | null>(null);

function useAccordion() {
  const context = useContext(AccordionContext);
  if (!context) {
    throw new Error(
      "Accordion compound components must be used within Accordion"
    );
  }
  return context;
}

// Main Accordion component
interface AccordionProps {
  children: React.ReactNode;
  defaultActiveIndex?: number | null;
  allowMultiple?: boolean;
}

function Accordion({
  children,
  defaultActiveIndex = null,
  allowMultiple = false,
}: AccordionProps) {
  const [activeIndex, setActiveIndex] = useState<number | null>(
    defaultActiveIndex
  );

  const handleSetActiveIndex = (index: number | null) => {
    if (allowMultiple) {
      // Implementation for multiple panels (would need array state)
      return;
    }
    setActiveIndex(activeIndex === index ? null : index);
  };

  return (
    <AccordionContext.Provider
      value={{ activeIndex, setActiveIndex: handleSetActiveIndex }}
    >
      <div className="accordion">{children}</div>
    </AccordionContext.Provider>
  );
}

// AccordionItem component
interface AccordionItemProps {
  children: React.ReactNode;
  index: number;
}

function AccordionItem({ children, index }: AccordionItemProps) {
  const { activeIndex } = useAccordion();
  const isActive = activeIndex === index;

  return (
    <div
      className={`accordion-item ${isActive ? "active" : ""}`}
      data-index={index}
    >
      {children}
    </div>
  );
}

// AccordionHeader component
interface AccordionHeaderProps {
  children: React.ReactNode;
}

function AccordionHeader({ children }: AccordionHeaderProps) {
  const { setActiveIndex } = useAccordion();
  const itemElement = useRef<HTMLElement>();

  useEffect(() => {
    // Find parent AccordionItem to get index
    let element = itemElement.current?.parentElement;
    while (element && !element.hasAttribute("data-index")) {
      element = element.parentElement;
    }
    itemElement.current = element as HTMLElement;
  }, []);

  const handleClick = () => {
    const index = itemElement.current?.getAttribute("data-index");
    if (index !== null && index !== undefined) {
      setActiveIndex(parseInt(index));
    }
  };

  return (
    <button
      ref={itemElement as any}
      className="accordion-header"
      onClick={handleClick}
      type="button"
    >
      {children}
    </button>
  );
}

// AccordionPanel component
interface AccordionPanelProps {
  children: React.ReactNode;
}

function AccordionPanel({ children }: AccordionPanelProps) {
  const { activeIndex } = useAccordion();
  const itemElement = useRef<HTMLElement>();
  const [isActive, setIsActive] = useState(false);

  useEffect(() => {
    let element = itemElement.current?.parentElement;
    while (element && !element.hasAttribute("data-index")) {
      element = element.parentElement;
    }

    if (element) {
      const index = parseInt(element.getAttribute("data-index") || "0");
      setIsActive(activeIndex === index);
    }
  }, [activeIndex]);

  return (
    <div
      ref={itemElement as any}
      className={`accordion-panel ${isActive ? "expanded" : ""}`}
      style={{
        display: isActive ? "block" : "none",
      }}
    >
      {children}
    </div>
  );
}

// Compound component assignment
Accordion.Item = AccordionItem;
Accordion.Header = AccordionHeader;
Accordion.Panel = AccordionPanel;

// Usage
function App() {
  return (
    <Accordion defaultActiveIndex={0}>
      <Accordion.Item index={0}>
        <Accordion.Header>What is React?</Accordion.Header>
        <Accordion.Panel>
          React is a JavaScript library for building user interfaces.
        </Accordion.Panel>
      </Accordion.Item>

      <Accordion.Item index={1}>
        <Accordion.Header>What is TypeScript?</Accordion.Header>
        <Accordion.Panel>
          TypeScript is a typed superset of JavaScript that compiles to plain
          JavaScript.
        </Accordion.Panel>
      </Accordion.Item>

      <Accordion.Item index={2}>
        <Accordion.Header>What are React Hooks?</Accordion.Header>
        <Accordion.Panel>
          Hooks are functions that let you use state and other React features
          without writing a class.
        </Accordion.Panel>
      </Accordion.Item>
    </Accordion>
  );
}
```

**Alternative implementation with better TypeScript support:**

```tsx
// More type-safe compound component approach
interface TabsContextType {
  activeTab: string;
  setActiveTab: (tabId: string) => void;
}

const TabsContext = createContext<TabsContextType | null>(null);

interface TabsProviderProps {
  children: React.ReactNode;
  defaultTab?: string;
}

function TabsProvider({ children, defaultTab = "" }: TabsProviderProps) {
  const [activeTab, setActiveTab] = useState(defaultTab);

  return (
    <TabsContext.Provider value={{ activeTab, setActiveTab }}>
      {children}
    </TabsContext.Provider>
  );
}

// Tab components
interface TabsProps {
  children: React.ReactNode;
  defaultTab?: string;
}

function Tabs({ children, defaultTab }: TabsProps) {
  return (
    <TabsProvider defaultTab={defaultTab}>
      <div className="tabs">{children}</div>
    </TabsProvider>
  );
}

interface TabListProps {
  children: React.ReactNode;
}

function TabList({ children }: TabListProps) {
  return (
    <div className="tab-list" role="tablist">
      {children}
    </div>
  );
}

interface TabProps {
  tabId: string;
  children: React.ReactNode;
  disabled?: boolean;
}

function Tab({ tabId, children, disabled = false }: TabProps) {
  const context = useContext(TabsContext);
  if (!context) throw new Error("Tab must be used within Tabs");

  const { activeTab, setActiveTab } = context;
  const isActive = activeTab === tabId;

  return (
    <button
      role="tab"
      aria-selected={isActive}
      aria-controls={`panel-${tabId}`}
      id={`tab-${tabId}`}
      className={`tab ${isActive ? "active" : ""}`}
      onClick={() => !disabled && setActiveTab(tabId)}
      disabled={disabled}
      type="button"
    >
      {children}
    </button>
  );
}

interface TabPanelsProps {
  children: React.ReactNode;
}

function TabPanels({ children }: TabPanelsProps) {
  return <div className="tab-panels">{children}</div>;
}

interface TabPanelProps {
  tabId: string;
  children: React.ReactNode;
}

function TabPanel({ tabId, children }: TabPanelProps) {
  const context = useContext(TabsContext);
  if (!context) throw new Error("TabPanel must be used within Tabs");

  const { activeTab } = context;
  const isActive = activeTab === tabId;

  return (
    <div
      role="tabpanel"
      id={`panel-${tabId}`}
      aria-labelledby={`tab-${tabId}`}
      className={`tab-panel ${isActive ? "active" : ""}`}
      hidden={!isActive}
    >
      {isActive ? children : null}
    </div>
  );
}

// Export compound component
const TabsCompound = Object.assign(Tabs, {
  List: TabList,
  Tab,
  Panels: TabPanels,
  Panel: TabPanel,
});

// Usage with proper TypeScript support
function TabExample() {
  return (
    <TabsCompound defaultTab="profile">
      <TabsCompound.List>
        <TabsCompound.Tab tabId="profile">Profile</TabsCompound.Tab>
        <TabsCompound.Tab tabId="settings">Settings</TabsCompound.Tab>
        <TabsCompound.Tab tabId="billing" disabled>
          Billing
        </TabsCompound.Tab>
      </TabsCompound.List>

      <TabsCompound.Panels>
        <TabsCompound.Panel tabId="profile">
          <h3>Profile Content</h3>
          <p>Manage your profile information here.</p>
        </TabsCompound.Panel>

        <TabsCompound.Panel tabId="settings">
          <h3>Settings Content</h3>
          <p>Adjust your application settings.</p>
        </TabsCompound.Panel>

        <TabsCompound.Panel tabId="billing">
          <h3>Billing Content</h3>
          <p>Manage your billing information.</p>
        </TabsCompound.Panel>
      </TabsCompound.Panels>
    </TabsCompound>
  );
}

export default TabsCompound;
```

**Benefits of Compound Components:**

- **Flexible API**: Users can compose components however they need
- **Separation of Concerns**: Each component has a single responsibility
- **Implicit State Sharing**: Context eliminates prop drilling
- **Type Safety**: TypeScript ensures correct usage

</details>

<details>
<summary>
    <h3>90. What is the Render Props pattern and how does it compare to custom hooks?</h3>
</summary>

Render Props is a pattern where a component accepts a function as a prop that returns React elements. This pattern enables component logic sharing and inversion of control.

**Render Props Implementation:**

```tsx
// Mouse position tracker using render props
interface MousePosition {
  x: number;
  y: number;
}

interface MouseTrackerProps {
  children: (mouse: MousePosition) => React.ReactNode;
  // Alternative: render prop
  render?: (mouse: MousePosition) => React.ReactNode;
}

class MouseTracker extends React.Component<MouseTrackerProps, MousePosition> {
  state: MousePosition = { x: 0, y: 0 };

  handleMouseMove = (event: MouseEvent) => {
    this.setState({
      x: event.clientX,
      y: event.clientY,
    });
  };

  componentDidMount() {
    window.addEventListener("mousemove", this.handleMouseMove);
  }

  componentWillUnmount() {
    window.removeEventListener("mousemove", this.handleMouseMove);
  }

  render() {
    const { children, render } = this.props;
    return (
      <div>
        {/* Use children function or render prop */}
        {render ? render(this.state) : children(this.state)}
      </div>
    );
  }
}

// Usage with children function
function App() {
  return (
    <MouseTracker>
      {({ x, y }) => (
        <div>
          <h1>Mouse Position</h1>
          <p>
            X: {x}, Y: {y}
          </p>
          <div
            style={{
              position: "absolute",
              left: x,
              top: y,
              width: 10,
              height: 10,
              backgroundColor: "red",
              borderRadius: "50%",
              pointerEvents: "none",
            }}
          />
        </div>
      )}
    </MouseTracker>
  );
}

// More complex render props example - Data fetcher
interface DataFetcherState<T> {
  data: T | null;
  loading: boolean;
  error: Error | null;
}

interface DataFetcherProps<T> {
  url: string;
  children: (state: DataFetcherState<T>) => React.ReactNode;
}

class DataFetcher<T> extends React.Component<
  DataFetcherProps<T>,
  DataFetcherState<T>
> {
  state: DataFetcherState<T> = {
    data: null,
    loading: true,
    error: null,
  };

  async componentDidMount() {
    await this.fetchData();
  }

  async componentDidUpdate(prevProps: DataFetcherProps<T>) {
    if (prevProps.url !== this.props.url) {
      await this.fetchData();
    }
  }

  fetchData = async () => {
    this.setState({ loading: true, error: null });

    try {
      const response = await fetch(this.props.url);
      if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
      }
      const data = await response.json();
      this.setState({ data, loading: false });
    } catch (error) {
      this.setState({
        error: error instanceof Error ? error : new Error("Unknown error"),
        loading: false,
      });
    }
  };

  render() {
    return this.props.children(this.state);
  }
}

// Usage
interface User {
  id: number;
  name: string;
  email: string;
}

function UserProfile({ userId }: { userId: number }) {
  return (
    <DataFetcher<User> url={`/api/users/${userId}`}>
      {({ data: user, loading, error }) => {
        if (loading) return <div>Loading user...</div>;
        if (error) return <div>Error: {error.message}</div>;
        if (!user) return <div>User not found</div>;

        return (
          <div>
            <h1>{user.name}</h1>
            <p>{user.email}</p>
          </div>
        );
      }}
    </DataFetcher>
  );
}
```

**Converting to Custom Hooks (Modern Approach):**

```tsx
// Custom hook version of mouse tracker
function useMousePosition(): MousePosition {
  const [mousePosition, setMousePosition] = useState<MousePosition>({
    x: 0,
    y: 0,
  });

  useEffect(() => {
    const handleMouseMove = (event: MouseEvent) => {
      setMousePosition({
        x: event.clientX,
        y: event.clientY,
      });
    };

    window.addEventListener("mousemove", handleMouseMove);
    return () => window.removeEventListener("mousemove", handleMouseMove);
  }, []);

  return mousePosition;
}

// Custom hook version of data fetcher
function useApi<T>(url: string): DataFetcherState<T> & { refetch: () => void } {
  const [state, setState] = useState<DataFetcherState<T>>({
    data: null,
    loading: true,
    error: null,
  });

  const fetchData = useCallback(async () => {
    setState((prev) => ({ ...prev, loading: true, error: null }));

    try {
      const response = await fetch(url);
      if (!response.ok) {
        throw new Error(`HTTP error! status: ${response.status}`);
      }
      const data = await response.json();
      setState({ data, loading: false, error: null });
    } catch (error) {
      setState({
        data: null,
        loading: false,
        error: error instanceof Error ? error : new Error("Unknown error"),
      });
    }
  }, [url]);

  useEffect(() => {
    fetchData();
  }, [fetchData]);

  return { ...state, refetch: fetchData };
}

// Usage with hooks (much cleaner!)
function App() {
  const mousePosition = useMousePosition();

  return (
    <div>
      <h1>Mouse Position</h1>
      <p>
        X: {mousePosition.x}, Y: {mousePosition.y}
      </p>
      <div
        style={{
          position: "absolute",
          left: mousePosition.x,
          top: mousePosition.y,
          width: 10,
          height: 10,
          backgroundColor: "red",
          borderRadius: "50%",
          pointerEvents: "none",
        }}
      />
    </div>
  );
}

function UserProfile({ userId }: { userId: number }) {
  const {
    data: user,
    loading,
    error,
    refetch,
  } = useApi<User>(`/api/users/${userId}`);

  if (loading) return <div>Loading user...</div>;
  if (error)
    return (
      <div>
        Error: {error.message}
        <button onClick={refetch}>Retry</button>
      </div>
    );
  if (!user) return <div>User not found</div>;

  return (
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
      <button onClick={refetch}>Refresh</button>
    </div>
  );
}
```

**Complex Render Props Example - Form Validation:**

```tsx
// Advanced render props for form validation
interface ValidationRules<T> {
  [K in keyof T]?: Array<(value: T[K]) => string | null>;
}

interface FormRenderProps<T> {
  values: T;
  errors: Partial<Record<keyof T, string>>;
  touched: Partial<Record<keyof T, boolean>>;
  handleChange: (field: keyof T) => (value: T[keyof T]) => void;
  handleBlur: (field: keyof T) => () => void;
  handleSubmit: (onSubmit: (values: T) => void) => (e: React.FormEvent) => void;
  isValid: boolean;
  isSubmitting: boolean;
}

interface FormProps<T> {
  initialValues: T;
  validationRules?: ValidationRules<T>;
  children: (props: FormRenderProps<T>) => React.ReactNode;
}

function Form<T extends Record<string, any>>({
  initialValues,
  validationRules = {},
  children
}: FormProps<T>) {
  const [values, setValues] = useState<T>(initialValues);
  const [errors, setErrors] = useState<Partial<Record<keyof T, string>>>({});
  const [touched, setTouched] = useState<Partial<Record<keyof T, boolean>>>({});
  const [isSubmitting, setIsSubmitting] = useState(false);

  const validateField = useCallback((field: keyof T, value: T[keyof T]): string | null => {
    const rules = validationRules[field];
    if (!rules) return null;

    for (const rule of rules) {
      const error = rule(value);
      if (error) return error;
    }
    return null;
  }, [validationRules]);

  const handleChange = useCallback((field: keyof T) => (value: T[keyof T]) => {
    setValues(prev => ({ ...prev, [field]: value }));

    if (touched[field]) {
      const error = validateField(field, value);
      setErrors(prev => ({ ...prev, [field]: error }));
    }
  }, [touched, validateField]);

  const handleBlur = useCallback((field: keyof T) => () => {
    setTouched(prev => ({ ...prev, [field]: true }));
    const error = validateField(field, values[field]);
    setErrors(prev => ({ ...prev, [field]: error }));
  }, [values, validateField]);

  const handleSubmit = useCallback((onSubmit: (values: T) => void) =>
    async (e: React.FormEvent) => {
      e.preventDefault();
      setIsSubmitting(true);

      // Validate all fields
      const newErrors: Partial<Record<keyof T, string>> = {};
      Object.keys(values).forEach(key => {
        const field = key as keyof T;
        const error = validateField(field, values[field]);
        if (error) newErrors[field] = error;
      });

      setErrors(newErrors);
      setTouched(
        Object.keys(values).reduce((acc, key) => ({
          ...acc,
          [key]: true
        }), {})
      );

      if (Object.keys(newErrors).length === 0) {
        try {
          await onSubmit(values);
        } catch (error) {
          console.error('Form submission error:', error);
        }
      }

      setIsSubmitting(false);
    }, [values, validateField]
  );

  const isValid = useMemo(() => {
    return Object.keys(values).every(key => {
      const field = key as keyof T;
      return !validateField(field, values[field]);
    });
  }, [values, validateField]);

  return (
    <>
      {children({
        values,
        errors,
        touched,
        handleChange,
        handleBlur,
        handleSubmit,
        isValid,
        isSubmitting
      })}
    </>
  );
}

// Usage
interface LoginForm {
  email: string;
  password: string;
}

const validationRules: ValidationRules<LoginForm> = {
  email: [
    (value) => value ? null : 'Email is required',
    (value) => /\S+@\S+\.\S+/.test(value) ? null : 'Email is invalid'
  ],
  password: [
    (value) => value ? null : 'Password is required',
    (value) => value.length >= 6 ? null : 'Password must be at least 6 characters'
  ]
};

function LoginPage() {
  const handleLogin = async (values: LoginForm) => {
    console.log('Logging in with:', values);
    // Simulate API call
    await new Promise(resolve => setTimeout(resolve, 1000));
  };

  return (
    <Form
      initialValues={{ email: '', password: '' }}
      validationRules={validationRules}
    >
      {({ values, errors, touched, handleChange, handleBlur, handleSubmit, isValid, isSubmitting }) => (
        <form onSubmit={handleSubmit(handleLogin)}>
          <div>
            <input
              type="email"
              placeholder="Email"
              value={values.email}
              onChange={(e) => handleChange('email')(e.target.value)}
              onBlur={handleBlur('email')}
            />
            {touched.email && errors.email && <span>{errors.email}</span>}
          </div>

          <div>
            <input
              type="password"
              placeholder="Password"
              value={values.password}
              onChange={(e) => handleChange('password')(e.target.value)}
              onBlur={handleBlur('password')}
            />
            {touched.password && errors.password && <span>{errors.password}</span>}
          </div>

          <button type="submit" disabled={!isValid || isSubmitting}>
            {isSubmitting ? 'Logging in...' : 'Login'}
          </button>
        </form>
      )}
    </Form>
  );
}
```

**Render Props vs Hooks Comparison:**

| Feature                | Render Props            | Custom Hooks         |
| ---------------------- | ----------------------- | -------------------- |
| **Syntax**             | More verbose            | Cleaner, simpler     |
| **Reusability**        | Good                    | Excellent            |
| **Composition**        | Nested functions        | Linear composition   |
| **TypeScript Support** | Complex generics        | Better inference     |
| **Performance**        | Can cause extra renders | More optimized       |
| **Learning Curve**     | Steeper                 | Easier               |
| **Modern React**       | Legacy pattern          | Recommended approach |

**When to Use Each:**

- **Render Props**: When you need very flexible component composition or working with class components
- **Custom Hooks**: For most modern React applications, simpler logic sharing, and better performance

</details>
