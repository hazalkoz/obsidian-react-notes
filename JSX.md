JSX is a JavaScript Extension Syntax used in React to easily write HTML and JavaScript together.

After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

**Warning:**
Since JSX is closer to JavaScript than to HTML, React DOM uses `camelCase` property naming convention instead of HTML attribute names.

Babel compiles JSX down to `React.createElement()` calls.


**JSX Limitations**

1. You can't return more than one "root" JSX element. (You also can't store more than one root JSX element in a variable.) Because in JS, functions can return a single thing. Each JSX element is converted to React.createElement(.....). ----> This can be solved with wrapping elements with other JSX elements such as a div, but you can end up with lots of wrappers. These are unnecessarly rendered in the DOM. 

Solution :  Create a helper wrapper component, and use [[Composition]]. Use this wrapper instead of div (or some other element) to avoid rendering any unnecessary elements.

``` javascript
const Wrapper = props => {
	return props.children;
};
```

⭐️  We don't have to create a wrapper component by using React's built-in [[Fragments]].