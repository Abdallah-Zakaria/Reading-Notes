# Classes, Inheritance

- **Why would you want to run JavaScript code outside of a browser?** For using node.js technology to execute your JavaScript code, This type of usage of javascript typically refers to backend programing where your javascript code will interact with your database and ccan used to create a restfull APIs.
- **What is the difference between a module and a package?**
    - A moodule is a single Javascript file that has some functionality.
    - A package is a directory with one or more modules inside of it and a package.json file which has matadata about the package.
- **What does the node package manager do?**
Node package manager is a command line tool that installs, updates or uninstalls Node.js packages in your application. and it's a repository for open source node. 
- **Provide code snippets showing 3 different ways to export a function from a node module**

1. export the function direct
```
module.exports = function(name){
    console.log(name)
}
```

1. export a variable function
```
let returnName = function(name){
    return `My name is ${name}`
}
module.exports = returnName()
```

1. export a value of a certian object 
```
let obj = {name : "someone" , age : 24}
module.exports = obj.name
```

## Document the following Vocabulary Terms:
- ecosystem : a community of organisms that live in and interact with each other in specific enviroment.
- Node.js : is a open source, cross plateform , javascript runtime enviroument that execute Javascript code outside the browser.
- v8 Engine : engine is a open source javascript that compiles javascript to optimized machine code before execution.
- A module : is a single javascript file that some resonable functionality.
- A package : is a directory with one more modules inside of it and a package.json file which has matadata about the package.
-  Node Package Manager : is a command line tool that installs, updates or uninstalls Node. js packages in your application. It is also an online repository for open-source Node.
- A server : is a computer that provides data for other computers. it may serve data systems on a local area network (LAN) or wide area network (WAN) over the internet.
- environment : the development environment is set proceses and programming tools used to create the programs written in a high-level language.
- compiler : is a special program that proceses statements written in particular programming language and turn them into machine language. 


### Inheritance with the prototype chain
JavaScript objects are dynamic "bags" of properties (referred to as own properties). JavaScript objects have a link to a prototype object. When trying to access a property of an object, the property will not only be sought on the object but on the prototype of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the prototype chain is reached.

```
// Let's create an object o from function f with its own properties a and b:
let f = function () {
   this.a = 1;
   this.b = 2;
}
let o = new f(); // {a: 1, b: 2}

// add properties in f function's prototype
f.prototype.b = 3;
f.prototype.c = 4;

// do not set the prototype f.prototype = {b:3,c:4}; this will break the prototype chain
// o.[[Prototype]] has properties b and c.
// o.[[Prototype]].[[Prototype]] is Object.prototype.
// Finally, o.[[Prototype]].[[Prototype]].[[Prototype]] is null.
// This is the end of the prototype chain, as null,
// by definition, has no [[Prototype]].
// Thus, the full prototype chain looks like:
// {a: 1, b: 2} ---> {b: 3, c: 4} ---> Object.prototype ---> null

console.log(o.a); // 1
// Is there an 'a' own property on o? Yes, and its value is 1.

console.log(o.b); // 2
// Is there a 'b' own property on o? Yes, and its value is 2.
// The prototype also has a 'b' property, but it's not visited. 
// This is called Property Shadowing

console.log(o.c); // 4
// Is there a 'c' own property on o? No, check its prototype.
// Is there a 'c' own property on o.[[Prototype]]? Yes, its value is 4.

console.log(o.d); // undefined
// Is there a 'd' own property on o? No, check its prototype.
// Is there a 'd' own property on o.[[Prototype]]? No, check its prototype.
// o.[[Prototype]].[[Prototype]] is Object.prototype and there is no 'd' property by default, check its prototype.
// o.[[Prototype]].[[Prototype]].[[Prototype]] is null, stop searching,
// no property found, return undefined.
```

### Inheriting "methods"
JavaScript does not have "methods" in the form that class-based languages define them. In JavaScript, any function can be added to an object in the form of a property.

```
var o = {
  a: 2,
  m: function() {
    return this.a + 1;
  }
};

console.log(o.m()); // 3
// When calling o.m in this case, 'this' refers to o

var p = Object.create(o);
// p is an object that inherits from o

p.a = 4; // creates a property 'a' on p
console.log(p.m()); // 5
// when p.m is called, 'this' refers to p.
// So when p inherits the function m of o, 
// 'this.a' means p.a, the property 'a' of p
```

### Function context
Inside a function, the value of this depends on how the function is called.
Since the following code is not in strict mode, and because the value of this is not set by the call, this will default to the global object, which is window in a browser.
```
function f1() {
  return this;
}

// In a browser:
f1() === window; // true

// In Node:
f1() === globalThis; // true
```

To set the value of this to a particular value when calling a function, use call(), or apply() as in the examples below.

### Class context
Unlike base class constructors, derived constructors have no initial this binding. Calling  super() creates a this binding within the constructor and essentially has the effect of evaluating the following line of code, where Base is the inherited class.

Referring to this before calling super() will throw an error.

```
// An object can be passed as the first argument to call or apply and this will be bound to it.
var obj = {a: 'Custom'};

// We declare a variable and the variable is assigned to the global window as its property.
var a = 'Global';

function whatsThis() {
  return this.a;  // The value of this is dependent on how the function is called
}

whatsThis();          // 'Global' as this in the function isn't set, so it defaults to the global/window object
whatsThis.call(obj);  // 'Custom' as this in the function is set to obj
whatsThis.apply(obj); // 'Custom' as this in the function is set to obj
```