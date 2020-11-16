# Props and State

#### Does a deployed React application require a server?
You don't necessarily need a static server in order to run a Create React App project in production.
#### Why do we prefer to test a React application at the behavior rather than the unit level?
Because the state change, that need to test it in many ways. 
#### What does npm run build do?
npm run build does nothing unless you specify what "build" does in your package.
#### Describe the actual composition / architecture of a React application


- **BDD** : behavior-driven development
- **Acceptance Tests** :technique performed to determine whether or not the software system has met the requirement specifications.
- **mounting** : one of the react life cycles that mean is when React "renders" the component for the first time and actually builds the initial DOM from those instructions.
- **build** : process of converting source code files into standalone software artifact(s) that can be run on a computer

### setState
setState() is the only legitimate way to update state after the initial state setup. Let’s say we have a search component and want to display the search term a user submits.

```js
import React, { Component } from 'react'

class Search extends Component {
  constructor(props) {
    super(props)

    state = {
      searchTerm: ''
    }
  }
}
```

```js
setState({ searchTerm: event.target.value })

```
![ex](https://i1.wp.com/css-tricks.com/wp-content/uploads/2018/04/image_preview-1.jpeg?w=645&ssl=1)

### Handling Events
Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

* React events are named using camelCase, rather than lowercase.
* With JSX you pass a function as the event handler, rather than a string.

```js
<button onClick={activateLasers}>
  Activate Lasers
</button>
```

When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. For example, this Toggle component renders a button that lets the user toggle between “ON” and “OFF” states:

```js
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState(state => ({
      isToggleOn: !state.isToggleOn
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}

ReactDOM.render(
  <Toggle />,
  document.getElementById('root')
);
```

### Forms
In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

```js
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
