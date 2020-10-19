# Express

### Review, Research, and Discussion
- **What’s the difference between PUT and PATCH?**
PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.

- **Provide links to 3 services or tools that allow you to “mock” an API for development**
- httpie
- Postman
- Swagger

- **Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?**
The OpenAPI is the official name of the specification. The development of the specification is fostered by the OpenAPI Initiative.
Swagger is the name associated with some of the most well-known, and widely used tools for implementing the OpenAPI specification. The Swagger toolset includes a mix of open source, free, and commercial tools, which can be used at different stages of the API lifecycle.

- **Compare and contrast SOAP and ReST**
- Meaning
  - SOAP : Simple Object Access Protocol
  - ReST : Representational State Transfer
- Approach
  - Function-driven
  - Data-driven
- Design
  - Standardized protocol with pre-defined rules to follow.
  - Architectural style with loose guidelines and recommendations.
- Security
  - WS-Security with SSL support. Built-in ACID compliance.
  - Supports HTTPS and SSL.

### Document the following Vocabulary Terms  
- **SOAP :** Simple Object Access Protocol is a messaging protocol specification for exchanging structured information in the implementation of web services in computer networks. Its purpose is to provide extensibility, neutrality, verbosity and independence.
- **ReST Verbs:** specify an action to be performed on a specific resource or a collection of resources.
- **CRUD Verbs:** The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operations, respectively. 
- **Swagger :** Swagger allows you to describe the structure of your APIs so that machines can read them. The ability of APIs to describe their own structure is the root of all awesomeness in Swagger

## Using middleware
Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

- Middleware functions can perform the following tasks:
  1. Execute any code.
  1. Make changes to the request and the response objects.
  1. End the request-response cycle.
  1. Call the next middleware function in the stack.

Types of middleware:
  - Application-level middleware
  - Router-level middleware
  - Error-handling middleware
  - Built-in middleware
  - Third-party middleware

## Routing
Routing refers to how an application’s endpoints (URIs) respond to client requests.
A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

- example of routes that are defined for the GET and the POST methods to the root of the app.
```
// GET method route
app.get('/', function (req, res) {
  res.send('GET request to the homepage')
})

// POST method route
app.post('/', function (req, res) {
  res.send('POST request to the homepage')
})
```

### Route paths
Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.

- examples of route paths based on strings

```
app.get('/', function (req, res) {
  res.send('root')
})
```

```
app.get('/about', function (req, res) {
  res.send('about')
})
```

```
app.get('/random.text', function (req, res) {
  res.send('random.text')
})
```

```
app.get('/ab*cd', function (req, res) {
  res.send('ab*cd')
})
```

```
app.get('/ab(cd)?e', function (req, res) {
  res.send('ab(cd)?e')
})
```
