# Hooks API  
#### Why do we not need more .html pages in a multi-page React app?
Because we build a react forntend client side that is a Single page Application, it's rerender the component that will render on the page not by render a new page.

#### If we wanted a component to show up on every page, where would we put it and why?
Inside the <BrowserRouter />, outside a <Route />

#### What does props.children contain?
props.children contains html tags passsed from the parent component to the child component and can access them from the child by {props.children}

- **Composition**	Composition is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props.
- **Children/child components**	Children components are given props from the parent component, and are rendered partially based on where they are in the parent component.
- **Hash Routing** Uses the hash in the URL to render the component. Since building a static one-page website, I needed to use this.
- **Link Routing**	Provides declarative, accessible navigation around your application.


### Hooks
We know that components and top-down data flow help us organize a large UI into small, independent, reusable pieces. However, we often can’t break complex components down any further because the logic is stateful and can’t be extracted to a function or another component. Sometimes that’s what people mean when they say React doesn’t let them “separate concerns.”

* Huge components that are hard to refactor and test.
* Duplicated logic between different components and lifecycle methods.
* Complex patterns like render props and higher-order components.

#### Do Hooks Make React Bloated?
Before we look at Hooks in detail, you might be worried that we’re just adding more concepts to React with Hooks. That’s a fair criticism. I think that while there is definitely going to be a short-term cognitive cost to learning them, the end result will be the opposite.


#### Effect Hook
You’ve likely performed data fetching, subscriptions, or manually changing the DOM from React components before. We call these operations “side effects” (or “effects” for short) because they can affect other components and can’t be done during rendering.

```js
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```
