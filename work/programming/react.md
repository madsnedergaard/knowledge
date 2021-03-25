---
description: 'Snippets, tips and ideas'
---

# React

WIP!



### Hooks

* Custom hooks - my most used ones goes here...



#### useReducer

The `useReducer` hook is great for managing complex local state instead of having a bunch of `useState` hooks that updates at the same time or depends on each other.

```javascript
const initialState = {count: 0};

const reducer = (state, action) => {
switch (action.type) {
    case 'increment':
    return {count: state.count + 1};
    case 'decrement':
    return {count: state.count - 1};
    default:
    throw new Error();
}
}

const Counter = () => {
const [state, dispatch] = useReducer(reducer, initialState);
return (
    <>
    Count: {state.count}
    <button onClick={() => dispatch({type: 'decrement'})}>-</button>
    <button onClick={() => dispatch({type: 'increment'})}>+</button>
    </>
);
}
```



