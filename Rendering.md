https://geekflare.com/react-rendering/

React maintains what’s called a [[Virtual DOM]] and that it periodically compares it with the actual [[DOM]] and applies changes as necessary.

⭐️ This is why you can’t just throw in jQuery and React together — React needs to take full control of the DOM.

Rendering is the React engine process walking through the [[Virtual DOM]] and collecting the current state, props, structure, desired changes in the UI, etc. 

React now updates the virtual DOM using some calculations and also compares the new result with the actual DOM on the page. This calculating and comparing is what the React team officially calls “reconciliation”.

Once the rendering part is done, React starts a phase called “commit”, during which it applies the necessary changes to the DOM. These changes are applied synchronously.

⭐️ Rendering means collecting info, and it doesn’t need to result in visual [[DOM]] changes every time. 
⭐️ What we consider as “rendering” is a two-step process involving rendering and commit.

Some changes in React can trigger [[Re-Rendering]].