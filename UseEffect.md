**Handling Side [[Effect]]s with useEffect**

```React
useEffect(()=>{...}, [dependencies]);
```

The first parameter of the useEffect hook is the function to be executed **AFTER** every component evaluation **IF** the specified **dependencies changed**. 

The second parameter is the list of the dependencies. If the list is empty, the function of this hook will be executed only once - when the component is mounted (rendered for the first time). If this parameter is missing, the function will be executed every time the component is re-rendered.

![[Pasted image 20220914003119.png]]
https://blog.bitsrc.io/understanding-dependencies-in-useeffect-7afd4df37c96

⭐️  UseEffect is an important hook that enables to deal with code that should be executed in response to something.

❗️ We should add all the things we use in our useEffect function, **if those things could change** because our component (or some parent component) re-rendered. 

⭐️  We can use UseEffect to implement [[Debouncing]] functionality.

   **Cleanup Function**
React’s useEffect cleanup function saves applications from unwanted behaviors like memory leaks by cleaning up effects. In doing so, we can optimize our application’s [[Performance]]. This function allows us to tidy up our code before our component unmounts. When our code runs and reruns for every render, useEffect also cleans up itself after using the cleanup function.

The useEffect Hook is built in a way that we can return a function inside it and this return function is where the cleanup happens.

``` JS
useEffect(() => {
        effect
        return () => {
            cleanup
        }
    }, [input])
```

⭐️  The cleanup function runs right before the execution of the next scheduled effect, and before unmounting the component. The cleanup is commonly used to cancel all subscriptions made and cancel fetch requests.

https://blog.logrocket.com/understanding-react-useeffect-cleanup-function/

Use effect can be optimized with [[Object Destructuring]], since we can get a specific property of complex states (as in [[UseReducer]] states).