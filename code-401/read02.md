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