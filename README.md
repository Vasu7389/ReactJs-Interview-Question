---
title: "Reactjs Interview Question 2023"
description: "Reactjs Interview Question 2023 with PDF download | Interview Questions for Reactjs and Redux"
---

<span style=" font-size: 0.8rem; border-bottom: 1px solid grey;"> Updated Dec 11, 2022 </span>

React has got more popularity among the top IT companies like Facebook, PayPal, Uber, etc., around the world.
Here you'll find the most frequently asked ReactJS and React Hooks interview questions that will help you in preparing your interview.

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
