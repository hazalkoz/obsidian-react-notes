Use UseReducer hook to handle more **complex states**, like multiple states are related with each other, there are multiple ways to change a state or it depends on other states. [[UseState]] becomes harder and more error-prone to use in such cases. UseReducer can be used as a **replacement** for useState when we need **more powerful state management**. But it is more complex to use, so we need to choose when to use reducers wisely. 

❗️ When some state depends on other states, the code have the possibility of not working properly, because of the scheduling algorithm of the react states.

An example:
```JS
setFormIsValid(
	event.target.value.includes('@') && enteredPassword.trim().length > 6
);
```

FormIsValid and enteredPassword are two different states. And setFormIsValid function may be executed before the enteredPassword state updates, so the validation will be falsely determined.

⭐️ It is a good use case to use reducer when we have states that belong together, and/or if we have state updates that depends on other state(s).

**UseReducer**
``` JS
const [state, dispatchFn] = useReducer(reducerFn, initialState, initFn);
```

_State_: The state snapshot is used in the component re-render/ re-evaluation cycle.
Dispatch Function: A function that can be used to dispatch a new action (i.e. trigger an update of the state). It will be consumed by the reducer function.

_Reducer Function_: A function that is triggered automatically once an action is dispatched (via dispatchFn()) it receives the latest state snapshot  and should return the new, updated state. Form: (prevState, action) => newState

_Initial State_: The initial state (optional)
_Initialization Function_: A function to set the initial state (optional)

Example:
	Checks an input field that accepts email, makes the field change color if the entered email is invalid.
``` JS
const emailReducer = (state, action) => {
	if (action.type === 'USER_INPUT'){
		return {value: action.val, isValid: action.val.includes('@')};
	}
	if (action.type === 'INPUT_BLUR'){
		return {value: state.value, isValid: state.value.includes('@')};
	}
	return {value: '', isValid: false};
}

const Login = (props) => {
	const [emailState, dispatchEmail] = useReducer(emailReducer, {
		value: '',
		isValid: null
	});

	const emailChangeHandler = (event) => {
		dispatchEmail({type: 'USER_INPUT', val: event.target.value});
	} 
	
	const validateEmailHandler = () => {
		dispatchEmail({type: 'INPUT_BLUR'});
	}
}
```

⭐️ Reducer function can be defined outside of the component, since it gets the newest state and action as parameters.