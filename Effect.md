**What is an Effect (Or Side Effect)**

The main job of the React library is rendering elements on the UI and changing the UI according to the user interactions. Some of the abilities that React provides are:
	- Evaluating and rendering JSX
	- Managing state and props
	- Reacting to user inputs and events
	- Re-evaluating components upon state and prop changes

Anything else that does not fit under the main job category is a side effect, such as:
	- Storing data in browser storage
	- Sending HTTP requests to backend
	- Setting and managing timers
etc.

These tasks must happen outside of the normal component evaluation and render cycle, because they can affect the [[Rendering]] behavior. For example, sending an HTTP request and using its response to change a state can cause an infinite loop; the request is sent, the response is now the new state, the component re-renders because of the state change, and sending HTTP request again. 

These side effects can be depenedent on some other element, state or prop. To handle the side effects (with their possible dependencies), we can use [[UseEffect]] hook.
