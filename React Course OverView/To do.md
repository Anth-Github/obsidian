C:\Users\Abel\Desktop\React_Projects\toDo\react-todo-list>

**Step 1: Setting up the project**

`npx create-react-app react-todo-list`  
`cd react-todo-list`  
`code .`  
`npm start`

This will open your default browser with the default React app running.

**Step 2: Clean up the initial files**

**Delete unnecessary files**

In the `src` folder, delete all files except `App.js`, `index.js`, and `index.css`.

**Update App.js**

Open `src/App.js` and replace its contents with:

Jsx

```
import React from 'react';

function App() {
  return (
    <div className="App">
      <h1>Todo List</h1>
    </div>
  );
}

export default App;
```

**Update index.js**

Open `src/index.js` and simplify it to:

Jsx

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

**Clear index.css**

Clear the contents of `src/index.css`.

Now you have a clean starting point for your todo list app. Your browser should show a page with just the "Todo List" heading.




Step 3: Implement Input for New Todos

1. First, let's update the `App.js` file to include state for the input:

```javascript
import React, { useState } from 'react';

function App() {
  const [inputValue, setInputValue] = useState('');

  const handleInputChange = (e) => {
    setInputValue(e.target.value);
  };

  return (
    <div className="App">
      <h1>Todo List</h1>
      <input
        type="text"
        value={inputValue}
        onChange={handleInputChange}
        placeholder="Enter a new todo"
      />
    </div>
  );
}

export default App;
```

This step introduces:

- A new state variable `inputValue` to hold the current input
- A `handleInputChange` function to update the input state
- An input field in the render method

Once you've made these changes, you should see an input field below the "Todo List" heading. You can type into it, but it won't do anything else yet.



Step 4: Implement Adding Todos

1. Update your `App.js` file with the following changes:


```javascript
import React, { useState } from 'react';

function App() {
  const [inputValue, setInputValue] = useState('');
  // New: Add state for todos
  const [todos, setTodos] = useState([]);

  const handleInputChange = (e) => {
    setInputValue(e.target.value);
  };

  // New: Add handleAddTodo function
  const handleAddTodo = () => {
    if (inputValue.trim() !== '') {
      setTodos([...todos, { id: Date.now(), text: inputValue }]);
      setInputValue('');
    }
  };

  return (
    <div className="App">
      <h1>Todo List</h1>
      <input
        type="text"
        value={inputValue}
        onChange={handleInputChange}
        placeholder="Enter a new todo"
      />
      {/* New: Add button to add todo */}
      <button onClick={handleAddTodo}>Add Todo</button>
      {/* New: Add unordered list to display todos */}
      <ul>
        {todos.map((todo) => (
          <li key={todo.id}>{todo.text}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```


The main changes in this step are:

1. Adding a new state variable `todos` to store the list of todo items.
2. Creating a new `handleAddTodo` function to add new todos to the list.
3. Adding a button in the JSX to trigger the `handleAddTodo` function.
4. Adding an unordered list in the JSX to display the todos.

These additions will allow you to add new todos and see them displayed in a list. Let me know if you need any clarification on these changes or when you're ready to move to the next step.



**Step 1: Create a new CSS file**

In the `src` folder, create a new file called `styles.css`. This file will contain all the styles for your app.

**Step 2: Import the CSS file**

In your `App.js` file, add the following line at the top to import the CSS file:

`import './styles.css';`

**Step 3: Add styles to the CSS file**

Open the `styles.css` file and add the following styles to get started:

CSS

```
.App {
  text-align: center;
  margin-top: 50px;
}

input[type="text"] {
  width: 300px;
  height: 30px;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  width: 100px;
  height: 30px;
  background-color: #4CAF50;
  color: #fff;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #3e8e41;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
  padding: 10px;
  background-color: #f0f0f0;
  border-radius: 5px;
}
```

These styles will give your app a basic layout and design. You can always add or modify styles as needed.

**Step 4: Save and check**

Save both files (`App.js` and `styles.css`) and check your app in the browser. You should see the styles applied to your Todo List app.

Let me know if you need help with anything else!


add gitignore. 