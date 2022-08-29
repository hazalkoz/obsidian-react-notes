[[Components]] can't just use data stored in other components.
Props are like attributes (properties) of HTML elements.

A parent component can send data to chil component as:

``` React
<ChildComponent prop1={sth} ... ></ChildComponent>
```

and the child component can reach them like:

```
export default function ChildComponent (props) {
	return <div>{props.prop1}</div>;
}
```

