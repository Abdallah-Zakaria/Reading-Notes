# Component Based UI

#### Name 5 Javascript UI Frameworks (other than React)
1. Vue
1. Angular
1. Ember
1. Backbone.js.

#### What’s the difference between a framework and a library?
When you use a library, you are in charge of the flow of the application. You are choosing when and where to call the library. When you use a framework, the framework is in charge of the flow. 

- **Rendering** : when add an element to the DOM 
- **Templates** : A template is a form, mold, or pattern used as a guide to making something and can be reused. 
- **State** : The state object is where you store property values that belongs to the component. When the state object changes, the component re-renders.

## React

#### code example:
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
* JSX may remind you of a template language, but it comes with the full power of JavaScript.
* JSX produces React “elements”.
* React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

#### Why JSX
* Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.

#### Embedding Expressions in JSX
```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```