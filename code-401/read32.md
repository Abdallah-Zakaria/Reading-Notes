# Custom Hooks

#### What does a component's lifecycle refer to?
This refers to the time from when a component mounts to when it unmounts. There are methods that you can call associated with this.

#### Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect?
because it fires a memoized version of the callback only if one of it's dependants has changed. This makes it faster and more efficient.

#### Why are functional components preferred over class components?
Functional components are less code, easier to read, perform better, and make it easier to separate components.


#### What is wrong with the following code?

```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```
useEffect should be outside of the for loop in this example.

### Custom Hooks
#### So How Do We Use Hooks
The easiest way to describe Hooks is to show side-by-side examples of a class component that needs to have access to state and lifecycle methods, and another example where we achieve the same thing with a functional component.

#### The Benefits of Using Hooks
Hooks have a lot of benefit to us as developers, and they are going to change the way we write components for the better.

#### Five Important Rules for Hooks
- Never call Hooks from inside a loop, condition or nested function
- Hooks should sit at the top-level of your component
- Only call Hooks from React functional components
- Never call a Hook from a regular function
- Hooks can call other Hooks
- React Hooks with Async-Await
- We cannot use ‘async’ keyword with ‘useEffect’ callback method. It will result in race conditions.