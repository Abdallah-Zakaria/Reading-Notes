# API Server
#### How does route prefixing work with an external routing module?
Route grouping is a concept to make the route function that receive same prefix of different requests. The route is being handle from route group.

#### When routing, what’s the difference between app.get(‘/data/:id’) and app.get(‘/data/:name’)? 
The diffrence in request pararms,  as the params is an object here have 2 property one for the name and the other for the id.
 
#### Explain how Express handles routing conflicts? 
Routes are processed by Express in order

#### What are the ways that a browser can send “data” or request variables to an HTTP server?
Using HTML tag form and pass the method of the request, path and the data if needed.

- **Routing :** How an application’s endpoints (URIs) respond to client requests.

- **Route Prefixing :**  Is a concept to make the route function that receive same prefix of different requests.

- **Request “Body” :** Property for request object comes with post,put,patch,delete method, here doesn't appears on the url

- **Request “Query” :** Property for request object comes with get method, here we send data in the url.

- **Request “Params” :** Property for request object comes with all method method t have placeholder in the url to send data on it.


## mongoose middleware
- Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions.

- **Types of Middleware**
  1. document middleware
  1. model middleware
  1. aggregate middleware
  1. query middleware.
  1. Use Cases
  1. Middleware are useful for atomizing model logic. Here are some other ideas:

 - **complex validation**
removing dependent documents (removing a user removes all his blogposts)
asynchronous defaults
asynchronous tasks that a certain action triggers
Post middleware
post middleware are executed after the hooked method and all of its pre middleware have completed.

## Subdocuments
Subdocuments are documents embedded in other documents. In Mongoose, this means you can nest schemas in other schemas.

Subdocuments versus Nested Paths
In Mongoose, nested paths are subtly different from subdocuments.

Finding a Subdocument
Each subdocument has an _id by default. Mongoose document arrays have a special id method for searching a document array to find a document with a given _id.