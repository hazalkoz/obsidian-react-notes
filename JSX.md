JSX is a JavaScript Extension Syntax used in React to easily write HTML and JavaScript together.

After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

**Warning:**
Since JSX is closer to JavaScript than to HTML, React DOM uses `camelCase` property naming convention instead of HTML attribute names.

Babel compiles JSX down to `React.createElement()` calls.