https://blog.logrocket.com/cleaning-up-the-dom-with-forwardref-in-react/#:~:text=React%20forwardRef%20is%20a%20method,anywhere%20it%20is%20being%20used.

https://blog.logrocket.com/complete-guide-react-refs/

Refs provide a way to access DOM nodes or React elements created in the render method.

Refs cannot be used on function components because they don't have instances. You may only use them on class components or DOM elements.

With refs, we can set up a connection between a HTML element (which is being rendered in the end) and our other JS code. The ref returns a value which allows us to work with that ref later, so we can reach the element that we are going to connect the ref.

⭐️  We can connect any HTML element to one of our references. We make the connection by using 'ref' prop.

⭐️  The ref will be holding the element that is rendered in the real DOM. The ref is always an object that has a 'current' prop that holds the actual value that the ref is connected.


❗️ The DOM should be manipulated only by React, so try to avoid using refs for manipulating the DOM.

❓ Use ref or state?
We can use both of them to keep track of the value of some element. Using refs may be easier if we will just read the value that the element keeps and we will not change it. The choice will affect if the component is a [[Controlled or Uncontrolled Component]].
