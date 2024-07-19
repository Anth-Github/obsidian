
2024-07-19 14:39

status:

Tags:

# Fundamentals of React.js

## Introduction to React.js

React.js is a JavaScript library for building user interfaces, developed and maintained by Facebook. It emphasizes the creation of reusable UI components, making it efficient and easy to develop complex UIs.

### Virtual DOM

- The **Virtual DOM** is a lightweight representation of the real DOM (Document Object Model).
- Changes in the Virtual DOM are compared with the previous state, and only the necessary updates are applied to the real DOM, resulting in efficient rendering.

### JSX Syntax

- **JSX (JavaScript XML)** is a syntax extension for JavaScript, which allows XML/HTML-like code to be written directly within JavaScript.
- It simplifies the creation of React elements and enhances readability.
- [[JSX]]
- 

### Component-Based Architecture

- React.js follows a **component-based architecture**, where UIs are divided into independent and reusable components.
- Each component manages its own state and can be composed together to build complex UIs.

## Core Concepts

### Components

- **Components** are the building blocks of React applications.
- They can be either **functional components** (using functions) or **class components** (using ES6 classes).
- Components can accept inputs called **props** and maintain their own internal state.

### State and Props

- **State** represents the data that a component maintains internally.
- **Props (Properties)** are inputs to a component that are passed from its parent component.
- **State** can be updated using `setState()`, triggering re-rendering of the component and its children.

### Lifecycle Methods

- **Lifecycle methods** are methods that are automatically invoked at specific points in a component's life.
- Examples include `componentDidMount()`, `componentDidUpdate()`, and `componentWillUnmount()`.
- They are used for initialization, data fetching, and cleanup operations.
- [[Lifecyclemethods]]

## Benefits of React.js

- **Declarative:** React makes it easy to build interactive UIs by describing how your UI should look.
- **Efficiency:** Virtual DOM and efficient rendering result in high performance.
- **Reusable Components:** Encourages the creation of reusable components, reducing redundancy and improving maintainability.



References
