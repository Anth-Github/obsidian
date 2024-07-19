
2024-07-19 15:31

status:

Tags:

# React Router

#### Introduction

React Router is a popular library for declaratively managing routing in React applications. It enables navigation among views or pages while maintaining a consistent user interface.

#### Installation

To install React Router in your project, use npm or yarn:

bash

Copy code

`npm install react-router-dom # or yarn add react-router-dom`

#### Basic Usage

1. **Router Setup**:
    
    - Wrap your application with `<BrowserRouter>` or `<HashRouter>` (for hash-based routing):
    
    javascript
    
    Copy code
    
    `import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';  function App() {   return (     <Router>       <div>         {/* Your application components here */}       </div>     </Router>   ); }`
    
2. **Route Declaration**:
    
    - Use `<Route>` component to define routes and specify which component should render for each route:
    
    javascript
    
    Copy code
    
    `function App() {   return (     <Router>       <div>         <Switch>           <Route exact path="/" component={Home} />           <Route path="/about" component={About} />           <Route path="/contact" component={Contact} />           <Route component={NotFound} />         </Switch>       </div>     </Router>   ); }`
    
    - `exact` attribute ensures that the route matches exactly, preventing partial matches.
3. **Navigation**:
    
    - Use `<Link>` component to navigate between routes:
    
    javascript
    
    Copy code
    
    `import { Link } from 'react-router-dom';  function Navbar() {   return (     <nav>       <ul>         <li><Link to="/">Home</Link></li>         <li><Link to="/about">About</Link></li>         <li><Link to="/contact">Contact</Link></li>       </ul>     </nav>   ); }`
    
    - `to` attribute specifies the target route.
4. **Nested Routes**:
    
    - Define nested routes using nested `<Route>` components:
    
    javascript
    
    Copy code
    
    `function App() {   return (     <Router>       <div>         <Switch>           <Route exact path="/" component={Home} />           <Route path="/products" component={Products} />           <Route path="/about" component={About} />         </Switch>       </div>     </Router>   ); }  function Products() {   return (     <div>       <h2>Products</h2>       <Switch>         <Route exact path="/products" component={ProductList} />         <Route path="/products/:id" component={ProductDetail} />       </Switch>     </div>   ); }`
    
    - Use `:parameter` syntax to capture dynamic segments of the URL.
5. **Redirects**:
    
    - Use `<Redirect>` to redirect to another route programmatically:
    
    javascript
    
    Copy code
    
    `import { Redirect } from 'react-router-dom';  function ProtectedRoute({ isLoggedIn, component: Component, ...rest }) {   return (     <Route       {...rest}       render={(props) =>         isLoggedIn ? (           <Component {...props} />         ) : (           <Redirect to="/login" />         )       }     />   ); }`
    

#### Additional Features

- **History Management**:
    
    - Access and manipulate the browser history using `useHistory` hook or `history` object provided by `<Router>`.
- **Route Parameters**:
    
    - Capture and access parameters from the URL using `useParams` hook or `match.params` in class components.
- **Programmatic Navigation**:
    
    - Use `history.push` or `history.replace` to navigate programmatically.

#### Conclusion

React Router simplifies navigation and routing in React applications, providing a powerful and flexible way to handle different views and states within your single-page applications. Mastering React Router allows for efficient and seamless navigation experiences for users.

References
