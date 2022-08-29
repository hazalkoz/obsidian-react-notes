In React, we can make components more generic by accepting [[Props]], which are to React components what parameters are to functions.

Component composition is the name for **passing components as props to other components**, thus creating new components with other components.

⭐️ props.children is a special prop which includes all the JSX elements between opening-closing tags of the component. 

Example of Component Composition :

```
export default function Card (props) {
	return <div>{props.children}</div>;
}

export default function ParentComponent (props) {
	return <Card>
		//some other elements
	</Card>
}
```

⭐️ The card is a wrapper component.

⭐️ The component composition can help with [[Prop Drilling]].

⭐️ Composition is also a great ally if you try to reduce the number of re-renders in your application, so it improves the [[Performance]].