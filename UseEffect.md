**Handling Side [[Effect]]s with useEffect**

```React
useEffect(()=>{...}, [dependencies]);
```

The first parameter of the useEffect hook is the function to be executed **AFTER** every component evaluation **IF** the specified **dependencies changed**. 

The second parameter is the list of the dependencies. If the list is empty, the function of this hook will be executed only once - when the component is mounted (rendered for the first time). If this parameter is missing, the function will be executed every time the component is re-rendered.

![[Pasted image 20220914003119.png]]
https://blog.bitsrc.io/understanding-dependencies-in-useeffect-7afd4df37c96







