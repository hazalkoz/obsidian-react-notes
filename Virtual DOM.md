(or React DOM in React)

React DOM takes care of updating the [[DOM]] to match the React elements.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

React elements are plain JS objects.

React elements are [immutable](https://en.wikipedia.org/wiki/Immutable_object). Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the [[User Interface]] at a certain point in time.
With our knowledge so far, the only way to update the UI is to create a new element, and pass it to `root.render()`.

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

