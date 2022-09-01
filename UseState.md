Call `useState()` hook to _enable state_ in a functional component.

The first argument of the `useState(initialValue)` is the state's _initial value_.

`[state, setState] = useState(initialValue)` returns an array of 2 items: the _state value_ and a state updater function.

Invoking the state updater function `setState(newState)` with the new value _updates the state_. Alternatively, you can invoke the state updater with a callback `setState(prev => next)`, which returns the new state based on previous.

After the state updater is called, React makes sure to _re-render_ the component so that the new state becomes actual.

