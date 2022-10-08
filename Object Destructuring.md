```JavaScript
const {isValid: emailIsValid } = emailState;

const [emailState, dispatchEmail] = useReducer(emailReducer, {
		value: '',
		isValid: null
	});

useEffect(()=>{
	//...function
}, [emailIsValid])
```

By using object destructuring, we get isValid property from emailState and used it as the dependency of [[useEffect]] hook.