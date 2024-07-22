The `useEffect` hook in React.js is a powerful feature that allows you to perform side effects in functional components. It is used for various purposes such as [[data fetching]], [[direct DOM manipulation]], [[setting up subscriptions]], and [[cleaning up resources]].
### Syntax 

```javascript
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // Your side effect code here
  }, [/* dependencies */]);

  return (
    <div>
      {/* Component JSX */}
    </div>
  );
}

```

### How `useEffect` Works

1. **Side Effects:** The code inside `useEffect` runs after the component renders. This is where you put side effects, such as fetching data from an API or manipulating the DOM.
2. **Dependencies Array:** The second argument to `useEffect` is an array of dependencies. The effect will run after the first render and only when any of the dependencies have changed.
    - **Empty Array (`[]`):** The effect runs only once after the initial render.
    - **No Array:** The effect runs after every render.
    - **Array with Dependencies:** The effect runs when any of the dependencies change.
### Example 1: Fetching Data 

```javascript
import React, { useEffect, useState } from 'react';

function DataFetchingComponent() {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data));
  }, []); // Empty array means this effect runs only once after the initial render

  return (
    <div>
      {data ? <pre>{JSON.stringify(data, null, 2)}</pre> : 'Loading...'}
    </div>
  );
}

```
 
### Example 2: Cleaning Up 


```javascript
import React, { useEffect } from 'react';

function TimerComponent() {
  useEffect(() => {
    const timer = setInterval(() => {
      console.log('Tick');
    }, 1000);

    // Cleanup function
    return () => {
      clearInterval(timer);
    };
  }, []); // Empty array means this effect runs only once after the initial render

  return (
    <div>
      Check the console for ticks every second.
    </div>
  );
}

```
 
### Example 3: Dependency Change 


```javascript
import React, { useState, useEffect } from 'react';

function CounterComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log('Count has changed to:', count);
  }, [count]); // Effect runs only when 'count' changes

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}

```
### Common Use Cases

- **Fetching Data:** Using `useEffect` to fetch data from APIs when the component mounts.
- **Subscribing to Events:** Adding event listeners when the component mounts and removing them when the component unmounts.
- **Updating Document Title:** Changing the document title based on component state or props.
- **Timers:** Setting up intervals or timeouts and clearing them when the component unmounts.
### Best Practices
- **Avoid Overuse:** Try to keep the logic inside `useEffect` minimal. Extract complex logic into separate functions.
- **Dependencies:** Always include all the dependencies that your effect relies on in the dependency array. This ensures that your effect is consistent and doesn't lead to unexpected behavior.
- **Cleanup:** Always return a cleanup function if your effect sets up any subscriptions or event listeners to prevent memory leaks.
### Summary
The `useEffect` hook is essential for managing side effects in React functional components. By understanding how to use it correctly, you can ensure your components are both efficient and free from bugs related to side effects.