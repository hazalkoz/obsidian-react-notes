Use UseReducer hook to handle more **complex states**, like multiple states are related with each other, there are multiple ways to change a state or it depends on other states. [[UseState]] becomes harder and more error-prone to use in such cases. UseReducer can be used as a **replacement** for useState when we need **more powerful state management**. But it is more complex to use, so we need to choose when to use reducers wisely. 

❗️ When some state depends on other states, the code have the possibility of not working properly, because of the scheduling algorithm of the react states.

An example:
```JS
setFormIsValid(
	event.target.value.includes('@') && enteredPassword.trim().length > 6
);
```

FormIsValid and enteredPassword are two different states. And setFormIsValid function may be executed before the enteredPassword state updates, so the validation will be falsely determined.

It is a good use case to use reducer when we have states that belong together, and/or if we have state updates that depends on other state(s).