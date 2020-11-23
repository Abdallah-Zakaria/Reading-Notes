# Context API

#### Describe use cases for useMemo() and useReducer()
useReducer() is useful when you need to use complex state logic, when you have mulitple sub values, or when the next state depends on the previous state. Use useMemo() runs during rendering, and it will only recompute the memoized value when one of its dependants has changed. This is an optimized way to avoid calculations every rerender.

#### Why do custom hooks need the use prefix?
It needs the prefix so that looking at it, you can immediately tell that it is a hook. Without this, it looks just like a regular function.

#### What do custom hooks usually do?
They give functionality that can be used across multiple components, and they are better than functions because they can access state and component lifecycle.

#### Using any list of custom hooks, research and name one that you think will be useful in your applications
react-use-form-state is a hook that helps maintain the state in different parts of an app. This could be really useful, as this has been a challenge in the ToDo app.

#### Describe how a hook that fetches API data might work
An API fetching hook would take in a url and any info necessary for the request and return the results of the API call. It could use a callback to update the state with the returned results.

**reducer**	This is a function that determines the changes to an application's state, using the action that it receives.


#### When to Use Context
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component:
```
class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

class ThemedButton extends React.Component {
  render() {
    return <Button theme={this.props.theme} />;
  }
}
```