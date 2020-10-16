# HTTP and REST
### Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.

Amman city in Jordan that located in Middle East

### What is the advantage of an ORM, like Mongoose?
- Productivity
- Application design
- Code Reuse
- Application Maintainability

### How does the repository pattern compare with an ORM?
Repositories deal with Domain/Business objects (from the app point of view), an ORM handles db objects. A business objects IS NOT a db object, first has behaviour, the second is a glorified DTO, it only holds data.

### When making a repository/facade, what flexibility do you gain?
The flexibility comes with if you need to move to another database layer later, you can code to an interface and then your application does not care what that initialization of that database layer is. It also makes testing a lot easier because then you can have a "TestingUsersRepository" that doesnt rely on anything but the class itself and your favorite js unit testing framework.

### Name 3 cloud based NoSQL Databases
1. Amazon DynamoDB
1. Oracle NoSQL Database Cloud Service
1. Amazon DocumentDB

## Document the following Vocabulary Terms
- **lifecycle** : Software Development Life Cycle is the application of standard business practices to building software applications. It’s typically divided into six to eight steps: Planning, Requirements, Design, Build, Document, Test, Deploy, Maintain. 

- **collection** : Collections same to tables in relational databases, and it's store documents.
- **the “Repository” design pattern** : Repository pattern is a kind of container where data access logic is stored. It hides the details of data access logic from business logic. In other words, we allow business logic to access the data object without having knowledge of underlying data access architecture.

- **mongoose middleware** : Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.

- **Object Relation Mapping (ORM)**: Object-relational-mapping is the idea of being able to write queries like this `SELECT * FROM users WHERE email = 'test@test.com';`, as well as much more complicated ones, using the object-oriented paradigm of your preferred programming language, and we are trying to interact with our database using our language of choice instead of SQL.


## Status Codes
With URLs and verbs, the client can initiate requests to the server. In return, the server responds with status codes and message payloads. The status code is important and tells the client how to interpret the server response. The HTTP spec defines certain number ranges for specific types of responses:

- **1xx: Informational Messages**
All HTTP/1.1 clients are required to accept the Transfer-Encoding header.

This class of codes was introduced in HTTP/1.1 and is purely provisional. The server can send a Expect: 100-continue message, telling the client to continue sending the remainder of the request, or ignore if it has already sent it. HTTP/1.0 clients are supposed to ignore this header.

- **2xx: Successful**
This tells the client that the request was successfully processed. The most common code is 200 OK. For a GET request, the server sends the resource in the message body. There are other less frequently used codes:

- 202 Accepted: the request was accepted but may not include the resource in the response. This is useful for async processing on the server side. The server may choose to send information for monitoring.
- 204 No Content: there is no message body in the response.
- 205 Reset Content: indicates to the client to reset its document view.
- 206 Partial Content: indicates that the response only contains partial content. Additional headers indicate the exact range and content expiration information.
- **3xx: Redirection**
404 indicates that the resource is invalid and does not exist on the server.

This requires the client to take additional action. The most common use-case is to jump to a different URL in order to fetch the resource.

- 301 Moved Permanently: the resource is now located at a new URL.
- 303 See Other: the resource is temporarily located at a new URL. The Location response header contains the temporary URL.
- 304 Not Modified: the server has determined that the resource has not changed and the client should use its cached copy. This relies on the fact that the client is sending ETag (Enttity Tag) information that is a hash of the content. The server compares this with its own computed ETag to check for modifications.

- **4xx: Client Error**
These codes are used when the server thinks that the client is at fault, either by requesting an invalid resource or making a bad request. The most popular code in this class is 404 Not Found, which I think everyone will identify with. 404 indicates that the resource is invalid and does not exist on the server. The other codes in this class include:

- 400 Bad Request: the request was malformed.
- 401 Unauthorized: request requires authentication. The client can repeat the request with the Authorization header. If the client already included the Authorization header, then the credentials were wrong.
- 403 Forbidden: server has denied access to the resource.
- 405 Method Not Allowed: invalid HTTP verb used in the request line, or the server does not support that verb.
- 409 Conflict: the server could not complete the request because the client is trying to modify a resource that is newer than the client's timestamp. Conflicts arise mostly for PUT requests during collaborative edits on a resource.

## What is REST
REST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems and was first presented by Roy Fielding in 2000 in his famous dissertation.

