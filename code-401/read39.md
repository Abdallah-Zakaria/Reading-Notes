# Redux - Additional Topics
#### What's the best practice for "pre-loading" data into the store (on application start) in a Redux application?
The best practice is to wrap the opening preload in useEffect. With this, you need to take the function outside of the props that you passed into the component.

#### When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
You will still be exporting the new data to replace the state from the reducer. The action calling the reducer will be sent as a function rather than an object.

**middleware In Redux**, middleware provides a third-party extention point between the when an action is dispatched and the moment it reaches the reducer. It needs to be used for asynchronous calls with Redux.
**thunk**	Thunk is a redux middleware that allows you to do async functions in conjunction with Redux.



## The core idea
State is the heart of each application and there is no quicker way to create buggy, unmanageable applications than by producing an inconsistent state or state that is out-of-sync with local variables that linger around. Hence many state management solutions try to restrict the ways in which you can modify state, for example by making state immutable. But this introduces new problems; data needs to be normalized, referential integrity can no longer be guaranteed and it becomes next to impossible to use powerful concepts like classes in case you fancy those.

MobX makes state management simple again by addressing the root issue: it makes it impossible to produce an inconsistent state. The strategy to achieve that is simple: Make sure that everything that can be derived from the application state, will be derived. Automatically.



* First of all, there is the application state. Graphs of objects, arrays, primitives, references that forms the model of your application. These values are the “data cells” of your application.
* Secondly there are derivations. Basically, any value that can be computed automatically from the state of your application. These derivations, or computed values, can range from simple values, like the number of unfinished todos, to complex stuff like a visual HTML representation of your todos. In spreadsheet terms: these are the formulas and charts of your application.
* Reactions are very similar to derivations. The main difference is these functions don't produce a value. Instead, they run automatically to perform some task. Usually this is I/O related. They make sure that the DOM is updated or that network requests are made automatically at the right time.
* Finally there are actions. Actions are all the things that alter the state. MobX will make sure that all changes to the application state caused by your actions are automatically processed by all derivations and reactions. Synchronously and glitch-free.