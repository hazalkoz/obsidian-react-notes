If a parent component in React changes (say, because its state ([[UseState]]) or [[Props]] changed), React walks the entire tree down this parent element and re-renders all components.

If your application has many nested components and a lot of interactions, you’re unknowingly taking a huge [[Performance]] hit every time you change the parent component (assuming it’s just the parent component you wanted to change).

Rendering won’t cause React to change the actual [[DOM]] because, during reconciliation, it will detect that nothing has changed for these components. But, it’s still CPU time and memory wasted.

