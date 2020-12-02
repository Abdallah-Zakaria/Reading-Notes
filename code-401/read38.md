# Redux - Asynchronous Actions

#### How granular should your reducers be?
There should be a separate reducer function for each slice of data. They are combined before being put into the store.

#### Pro or Con - multiple reducers can "fire" when a commonly named action is dispatched
This is a Con because you may fire off reducers that you did not intend.

#### Name a strategy for preventing the above
You can use more specific names that represent the reducer and data want to change .

**store**	This holds the state of the application. This can only be changed when actions are dispatched to the store.
**combined reducers**	This takes all the reducer functions from an app and combines them to pass to createStore.


## Redux Middleware and Side Effects#
By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:

* Logging a value to the console
* Saving a file
* Setting an async timer
* Making an AJAX HTTP request
* Modifying some state that exists outside of a function, or mutating arguments to a function
* Generating random numbers or unique random IDs (such as Math.random() or Date.now())