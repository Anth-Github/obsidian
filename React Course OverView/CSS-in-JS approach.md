The CSS-in-JS approach is a methodology in which CSS styles are written in JavaScript files, alongside the components that use them. This approach has gained popularity with the rise of modern front-end frameworks like React, Next.js, and Vue.js.

Key benefits of CSS-in-JS:

1. Scoped styles: Styles are scoped to the component, reducing the risk of global CSS conflicts.
2. Easy maintenance: Styles are co-located with the component, making it easier to maintain and update.
3. Dynamic styling: Styles can be dynamically generated based on props, state, or other conditions.
4. No CSS files: No need to manage separate CSS files, reducing complexity.
5. Improved performance: Styles are only loaded when the component is rendered, reducing unnecessary CSS.

Popular CSS-in-JS libraries:

1. Styled Components: A popular library for React and Next.js.
2. Emotion: A library for React, Next.js, and Vue.js.
3. Glamor: A library for React and Next.js.

Example of CSS-in-JS with Styled Components:


```javascript
import styled from 'styled-components';

const Button = styled.button`
  background-color: ${props => props.primary ? 'blue' : 'gray'};
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
`;

function MyComponent() {
  return <Button primary>Click me!</Button>;
}
```

In this example, the Button component is styled using the styled function from Styled Components. The styles are defined in the JavaScript file, and the primary prop is used to dynamically change the background color.