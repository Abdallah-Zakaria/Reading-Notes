# Redux - Combined Reducers
#### Why choose Redux instead of the Context API for global state?
Redux is the industry standard for managing state of large applications, so it is important to know well. It is more optimized for larger projects, because the context API rerenders more often.

#### What is the purpose of a reducer?
We need reducers to tell the application how to change state in response to an action. The action does not do anything except describe what happended and it is up to the reducer to respond to this.

#### What does an action contain?
An action contains a type and whatever payload you want it to have.

#### Why do we need to copy the state in a reducer?
The reducer needs to be a pure function without any side-effects. It should only take in an action and return the new state.

**immutable state**	This allows the state to only change when absolutely necessary to make React apps perform as well as possible.
**time travel in redux**	This is a feature of redux dev tools that allows you to see every state that a page has been in.
**action creator**	Actions send data from your application to your store, and are the only source of information for the store. An action creator is a function that creates an action.
**reducer**	Reducers tell the application how to change state in response to an action.
**dispatch**	This is the name of the function you use to send actions to the store.


## Using combineReducers
#### Core Concepts
The most common state shape for a Redux app is a plain Javascript object containing "slices" of domain-specific data at each top-level key. Similarly, the most common approach to writing reducer logic for that state shape is to have "slice reducer" functions, each with the same (state, action) signature, and each responsible for managing all updates to that specific slice of state. Multiple slice reducers can respond to the same action, independently update their own slice as needed, and the updated slices are combined into the new state object.

Because this pattern is so common, Redux provides the combineReducers utility to implement that behavior. It is an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function.

There are several important ideas to be aware of when using combineReducers:

* First and foremost, combineReducers is simply a utility function to simplify the most common use case when writing Redux reducers. You are not required to use it in your own application, and it does not handle every possible scenario. It is entirely possible to write reducer logic without using it, and it is quite common to need to write custom reducer logic for cases that combineReducer does not handle. (See Beyond combineReducers for examples and suggestions.)
* While Redux itself is not opinionated about how your state is organized, combineReducers enforces several rules to help users avoid common errors. (See combineReducers for details.)
* One frequently asked question is whether Redux "calls all reducers" when dispatching an action. Since there really is only one root reducer function, the default answer is "no, it does not". However, combineReducers has specific behavior that does work that way. In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.
* You can use it at all levels of your reducer structure, not just to create the root reducer. It's very common to have multiple combined reducers in various places, which are composed together to create the root reducer.