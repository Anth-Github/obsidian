- This file is a CSS Module, which means its styles are scoped to a specific component (in this case, the Home component).
- Any styles you write in home.module.css will only be applied to the Home component.
- Use this file for:
    - Component-specific styles
    - Styles that are unique to the Home component
    - Overriding global styles for this specific component

Using both files allows you to:

- Keep global styles separate from component-specific styles
- Avoid naming conflicts or unintended style overrides
- Write more modular and maintainable CSS code

By using CSS Modules (like home.module.css), you can also take advantage of features like:

- Automatic class name generation (e.g., home_module__header__1r4bz)
- Easy debugging and inspection in the browser dev tools