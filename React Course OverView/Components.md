
**1. What are Components?**

- **Definition**: Components are the building blocks of a React application. They encapsulate a part of the user interface (UI) and manage its ***logic and state.***
- **Purpose**: They allow you to split the UI into reusable, manageable pieces, making development more modular and maintainable.
### **Types of Components**

**1. Functional Components**

- **Definition**: Simple JavaScript functions that accept `props` as arguments and return React elements.
- **Syntax**:
    `function MyComponent(props) {   return <div>{props.message}</div>; }`
    
- **Features**:
    - Stateless by default, though hooks can be used to manage state and side effects.
    - Ideal for presentational components and when no internal state or lifecycle methods are needed.

**2. Class Components** {***are not so widely used, can be ignored for now.}

- **Definition**: ES6 classes that extend `React.Component` and require a `render()` method.
- **Syntax**:

    `class MyComponent extends React.Component {   render() {     return <div>{this.props.message}</div>;   } }`
    
- **Features**:
    - Can manage local state and use lifecycle methods.
    - Suitable for more complex components requiring internal state and lifecycle methods.

### **Key Concepts in Components**

**1. Props (Properties)**

- **Definition**: Read-only data passed from a parent component to a child component.
- **Usage**: Used to configure and customize components.
- **Example**: 
    `<Greeting name="John" />`
    
    In `Greeting` component:
        `function Greeting(props) {   return <h1>Hello, {props.name}!</h1>; }`
    
**2. State**

- **Definition**: Mutable data managed within a component.
- **Usage**: Allows a component to maintain its own data and re-render when the state changes.
- **Functional Components**: Use the `useState` hook. 

```javascript
import React, { useState } from 'react';  
function Counter() {   
const [count, setCount] = useState(0);  
return (     
<div>       
<p>Count: {count}</p>       
<button onClick={() => setCount(count + 1)}>Increment</button>     
</div>   ); 
}
```
 
**3. Lifecycle Methods**

- **Definition**: Special methods in class components that allow you to hook into different phases of a component's lifecycle.
- **Common Methods**:
    - `componentDidMount()`: Called after the component is mounted.
    - `componentDidUpdate(prevProps, prevState)`: Called after the component updates.
    - `componentWillUnmount()`: Called before the component is removed from the DOM.
- **Functional Components**: Use the `useEffect` hook to handle lifecycle events. 

```javascript
import React, { useEffect } from 'react';  
function MyComponent() {   
useEffect(() => {     // Code to run on mount     
return () => {       // Cleanup code     
};   }, []); 
return 
<div>My Component</div>; 
}
```
     
**4. JSX (JavaScript XML)**

- **Definition**: A syntax extension for JavaScript that looks similar to HTML and is used to describe the UI structure.
- **Usage**: Allows you to write HTML elements and components in a JavaScript file.
- **Example**: 

```javascript
function App() {   
return (     
<div>       
<h1>Hello, World!</h1>       
<p>Welcome to React.</p>     
</div>  
); 
}
```
    
**5. Conditional Rendering**

- **Definition**: Rendering different UI elements based on certain conditions.
- **Usage**: Use conditional statements inside JSX to render different components or elements.

**Example**: 

```javascript
function Welcome(props) {   
if (props.isLoggedIn) 
{     return <UserProfile />;   } 
else 
{     return <Login />;   } 
}
```
    
**6. Lists and Keys**

- **Definition**: Rendering lists of items and using keys to identify elements.
- **Usage**: Helps in rendering arrays of data and keeping track of items.
**Example**: 

```javascript
function ItemList(props) {   
return (     
<ul>       {props.items.map(item => (         
			<li key={item.id}>{item.name}</li>       
			))}    
 </ul>   ); 
 }
```

### **Summary**

- **Functional Components**: Simple, stateless, use hooks for state and lifecycle.
- **Class Components not very important repeating again. **: Can manage state and use lifecycle methods, more complex.
- **Props**: Read-only data passed to components.
- **State**: Mutable data managed within a component.
- **Lifecycle Methods**: Special methods to hook into different phases of a component’s lifecycle.
- **JSX**: Syntax extension that allows writing HTML-like code in JavaScript.
- **Conditional Rendering**: Render different UI elements based on conditions.
- **Lists and Keys**: Efficiently render lists and track elements.

Components in React allow for modular, maintainable, and efficient user interface development, leveraging reusable parts and managing UI updates effectively.