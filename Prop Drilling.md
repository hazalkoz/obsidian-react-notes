Prop drilling is the act of **passing [[Props]] through multiple layers of components**.

Here's an example where we are passing `userName` through multiple layers:

```jsx
const App = () => {
  const userName = 'Joe';

  return (
    <WelcomePage userName={userName} />
  );
}

const WelcomePage = ({ userName }) => {
  return (
    <>
      <WelcomeMessage userName={userName} />
      {/** Some other welcome page code */}
    </>
  );
}

const WelcomeMessage = ({ userName }) => {
  return (
    <h1>Hey, {userName}!</h1>
  );
}
```

App passes `userName` to WelcomePage, and WelcomePage passes `userName` to WelcomeMessage.

With only a few layers, this isn't a big deal, but this can quickly get out of hand in larger applications and it affects [[Performance]] badly.

Instead of passing `userName` through all these layers, we can try to compose the components at a higher level, like the `App` component.

``` jsx
const App = () => { 
	const userName = 'Joe'; 
	return ( 
		<WelcomePage title={<WelcomeMessage userName={userName} />} /> 
	); 
} 

const WelcomePage = ({ title }) => { 
	return ( <> {title} {/** Some other welcome page code */} </> );
} 
	
const WelcomeMessage = ({ userName }) => { return ( <h1>Hey, {userName}!</h1> ); }

```
