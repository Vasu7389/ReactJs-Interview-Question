---
title: "Reactjs Interview Question 2023"
description: "Reactjs Interview Question 2023 with PDF download | Interview Questions for Reactjs and Redux"
---

<span style=" font-size: 0.8rem; border-bottom: 1px solid grey;"> Updated Dec 2, 2022 </span>

<details>
<summary>
    <h3>1. Write a custom hook which can be used for debouncing feature.</h3> 
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
    <h3>2. Write a custom hook which can be used to copy text to clipboard.</h3> 
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
