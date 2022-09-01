**Why were React hooks created?**

Class-based components were not working out:
- Classes are a lie (of the “damned” type) in JavaScript. When a JavaScript engine runs code, it has no notion of classes; thus, a tool like [Babel](https://babeljs.io/) is needed to convert “modern”, “nice-looking” classes into plain functions. If there’s inheritance involved, it gets converted to the _only_ type of inheritance possible in JavaScript — [Prototypal Inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain).
- Classes might promote code reuse in other contexts (and languages), but in React, they introduce problems in code sharing.
- [[Prop Drilling]] issue was solved by [[Redux]] but it is too much upfront investment if you’re not going to use Redux for everything.

Hooks are not aimed at any one thing but are a major paradigm shift.

Hooks are a way of writing React [[Components]] without classes; they also provide you ways to “hook” into the React core features such as state, controlling [[Re-Rendering]]s, etc., in functional components.

They simplify the component structure, architecture, hierarchy, code reuse, and much more.

[Basic Hooks](https://reactjs.org/docs/hooks-reference.html#basic-hooks)
    
 - [[UseState]](https://reactjs.org/docs/hooks-reference.html#usestate)
 - [[UseEffect]](https://reactjs.org/docs/hooks-reference.html#useeffect)
 -  [`useContext`](https://reactjs.org/docs/hooks-reference.html#usecontext)

- [Additional Hooks](https://reactjs.org/docs/hooks-reference.html#additional-hooks)
    
    -   [`useReducer`](https://reactjs.org/docs/hooks-reference.html#usereducer)
    -   [[UseCallback]](https://reactjs.org/docs/hooks-reference.html#usecallback)
    -   [`useMemo`](https://reactjs.org/docs/hooks-reference.html#usememo)
    -   [[UseRef]](https://reactjs.org/docs/hooks-reference.html#useref)
    -   [`useImperativeHandle`](https://reactjs.org/docs/hooks-reference.html#useimperativehandle)
    -   [`useLayoutEffect`](https://reactjs.org/docs/hooks-reference.html#uselayouteffect)
    -   [`useDebugValue`](https://reactjs.org/docs/hooks-reference.html#usedebugvalue)
    -   [`useDeferredValue`](https://reactjs.org/docs/hooks-reference.html#usedeferredvalue)
    -   [`useTransition`](https://reactjs.org/docs/hooks-reference.html#usetransition)
    -   [`useId`](https://reactjs.org/docs/hooks-reference.html#useid)

