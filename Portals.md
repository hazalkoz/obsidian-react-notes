  We can use portals to render HTML elements in a different place (other than it would normally be rendered) in the real [[DOM]] without changing the structure of the JSX.

To add a portal:
1. Go to index.html, create a div for the portal destination (where the element will be rendered), give it some id.
2. import ReactDOM from 'react-dom'
3. Create portal with ReactDOM.createProtal(React node, pointer to the destination container) method in JSX code. 


Ex:

``` JSX
return (
	<>
		{ReactDOM.createPortal(<Backdrop onClick={...}/>, document.getELementById('backdrop-root'))}
	</>
)
```
