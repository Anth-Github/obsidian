
2024-07-19 15:35

status:

Tags:

# Hooks for functional components
### State Hooks

#### useState

`useState` is used for managing state within functional components. It allows you to declare state variables and update functions directly within the function body.

**Example: Counter Component**

 Copy code

```javascript
 import React, { useState } from 'react';

function Counter() {
  // Declare a state variable 'count' initialized to 0
  const [count, setCount] = useState(0);

  // Event handler to increment count
  const increment = () => {
    setCount(count + 1); // Update count using setCount function
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}

export default Counter;

```
 

- **Explanation**:
    - `useState(0)` initializes the state variable `count` with an initial value of `0`.
    - `setCount` is a function provided by `useState` to update the `count` state.
    - `increment` is an event handler that calls `setCount` to increment `count` by 1.

#### useReducer

`useReducer` is an alternative to `useState` for managing more complex state logic. It accepts a reducer function and an initial state, and returns the current state and a dispatch function.

**Example: Counter Component with useReducer**

 
Copy code
```javascript
import React, { useReducer } from 'react';

// Initial state for the reducer
const initialState = { count: 0 };

// Reducer function that specifies how state updates in response to actions
function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return { count: state.count + 1 };
    case 'decrement':
      return { count: state.count - 1 };
    default:
      throw new Error();
  }
}

function Counter() {
  // useReducer returns current state and dispatch function
  const [state, dispatch] = useReducer(reducer, initialState);

  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={() => dispatch({ type: 'increment' })}>Increment</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button>
    </div>
  );
}

export default Counter;

```

- **Explanation**:
    - `useReducer(reducer, initialState)` initializes state with `initialState` and uses `reducer` to handle state updates.
    - `state.count` holds the current count value.
    - `dispatch` is used to dispatch actions (`{ type: 'increment' }` and `{ type: 'decrement' }`) to the reducer, which updates the state based on the action type.

### Effect Hooks

#### useEffect

`useEffect` is used to perform side effects in functional components. It's similar to `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` combined in class components.

**Example: DataFetcher Component**

javascript

Copy code

 ```javascript
 import React, { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState(null);

  // useEffect to fetch data when component mounts
  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch('https://api.example.com/data');
        const result = await response.json();
        setData(result);
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    };

    fetchData(); // Invoke fetchData function
  }, []); // empty dependency array means run once on mount

  return (
    <div>
      {data ? (
        <ul>
          {data.map(item => (
            <li key={item.id}>{item.name}</li>
          ))}
        </ul>
      ) : (
        <p>Loading...</p>
      )}
    </div>
  );
}

export default DataFetcher;

```

- **Explanation**:
    - `useEffect` accepts a function (`fetchData`) that contains code for fetching data.
    - `fetchData` is invoked when the component mounts (`[]` as dependency array ensures it runs only once).
    - `setData` updates the component state (`data`) with the fetched data, triggering a re-render to display the data.

#### useLayoutEffect

`useLayoutEffect` is similar to `useEffect`, but it runs synchronously after all DOM mutations. It's used when you need to perform DOM measurements or actions that need to be reflected synchronously before the browser paints.

### Other Hooks

#### useContext

`useContext` is used to consume values from a context created by `React.createContext`.

**Example: Consuming Context in a Component**

 
```javascipt
import React, { useContext } from 'react';
import MyContext from './MyContext'; // Assume MyContext is a created context

function MyComponent() {
  const value = useContext(MyContext); // Access context value

  return <p>Context Value: {value}</p>;
}

export default MyComponent;
```

 
- **Explanation**:
    - `useContext(MyContext)` retrieves the current context value provided by the nearest `<MyContext.Provider>` component in the component tree.

#### useMemo and useCallback

`useMemo` and `useCallback` are used for optimizing performance by memoizing expensive computations and functions.

**Example: Memoizing Expensive Component** 

```javascript
import React, { useMemo, useCallback } from 'react';

function ExpensiveComponent({ data }) {
  // useMemo memoizes the result of computeExpensiveValue function
  const expensiveValue = useMemo(() => computeExpensiveValue(data), [data]);

  // useCallback memoizes the handleClick function
  const handleClick = useCallback(() => {
    // handle click logic
  }, []); // empty dependency array means function is memoized

  return (
    <div>
      <p>Expensive Value: {expensiveValue}</p>
      <button onClick={handleClick}>Click me</button>
    </div>
  );
}

export default ExpensiveComponent;
```

- **Explanation**:
    - `useMemo(() => computeExpensiveValue(data), [data])` computes `expensiveValue` only when `data` changes, optimizing performance.
    - `useCallback(() => {...}, [])` memoizes `handleClick` function, preventing unnecessary re-creation on re-renders unless dependencies change.

### Custom Hooks

Custom hooks are user-defined hooks that abstract stateful logic into reusable functions.

**Example: Custom Hook for Window Width**


```javascript
import { useState, useEffect } from 'react';

function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener('resize', handleResize);
    return () => {
      window.removeEventListener('resize', handleResize);
    };
  }, []);

  return width;
}

export default useWindowWidth;

```

**Explanation**:

- `useWindowWidth` custom hook encapsulates logic for tracking window width using `useState` and `useEffect`.
- Returns `width` state and handles cleanup by removing resize event listener on component unmount.

Using the Custom Hook in a Component:

```javascript
import React from 'react';
import useWindowWidth from './useWindowWidth';

function WindowWidthComponent() {
  const width = useWindowWidth(); // Custom hook to get window width

  return <p>Window width is: {width}</p>;
}

export default WindowWidthComponent;

```


- **Explanation**:
    - `useWindowWidth` hook is imported and used in `WindowWidthComponent`, allowing the component to display and update `width` dynamically based on window resize events.

### Conclusion

Hooks provide a more straightforward and efficient way to manage stateful logic and side-effects within functional components in React. By understanding and utilizing these hooks effectively, you can improve code readability, maintainability, and performance in your React applications. Each hook serves a specific purpose and can be combined to create sophisticated UI components while adhering to React's declarative and composable programming model.

asdfasdf
 