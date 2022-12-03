---
title: "Reactjs Interview Question 2023"
description: "Reactjs Interview Question 2023 with PDF download | Interview Questions for Reactjs and Redux"
---

<span style=" font-size: 0.8rem; border-bottom: 1px solid grey;"> Updated Dec 2, 2022 </span>

<details>
<summary>
    <h3>1. Write a custom hook which can be used to debounce user's input.</h3> 
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
    <h3>2. Write a custom hook to copy text to clipboard.</h3> 
</summary>

```jsx
//helper method
const copyToClipboard = (str) => {
  const elmnt = document.createElement("textarea");
  elmnt.value = str;
  elmnt.setAttribute("readonly", "");
  elmnt.style.position = "absolute";
  elmnt.style.left = "-9999px";
  document.body.appendChild(elmnt);
  const selected =
    document.getSelection().rangeCount > 0
      ? document.getSelection().getRangeAt(0)
      : false;
  elmnt.select();
  const success = document.execCommand("copy");
  document.body.removeChild(elmnt);
  if (selected) {
    document.getSelection().removeAllRanges();
    document.getSelection().addRange(selected);
  }
  return success;
};

//hook
const useCopyToClipboard = (text) => {
  const [copied, setCopied] = useState(false);

  const copy = useCallback(() => {
    if (!copied) setCopied(copyToClipboard(text));
  }, [text]);

  useEffect(() => () => setCopied(false), [text]);

  return [copied, copy];
};

//usage
const TextCopy = (props) => {
  const [copied, copy] = useCopyToClipboard("Text to copy!");
  return (
    <div>
      <button onClick={copy}>Click to copy</button>
      <span>{copied && "Copied!"}</span>
    </div>
  );
};
```

</details>

<details>
<summary>
    <h3>3. How to Use the 'useId' Hook to generate unique ids.</h3> 
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
    <h3>4. How to validate Props in React?</h3> 
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
    <h3>5. Give a practical example of Higher Order Component in react.</h3> 
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
    <h3>6. Why React's useDeferredValue hook is useful?</h3> 
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
    <h3>7. How to detect 'click' outside React component?</h3> 
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
    <h3>8. Why do React component names have to start with capital letters?</h3> 
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
    <h3>9. What is the difference between npx and npm?</h3> 
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
    <h3>10. How to set focus on an input field after component mounts on UI?</h3> 
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
