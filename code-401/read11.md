# Authentication
#### Explain what a “Singleton” is (in Computer Science terms)
Used where only a single instance of a class is required to control the action throughout an execution.
#### Explain how the Singleton pattern can be used with Node modules, specifically with classes
Create a single object to use with other objects without having to recreate that object multiple times. It allows us to uses one instance of an object through out different objects.
#### f you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
Select types of middleware I need to create .

- **Router Middleware:** Middleware functions are functions that have access to the request object, the response object.
- **Dynamic Module Loading:** Dynamic call a module only once vs static which call modules twice.
- **Singleton Pattern:** A software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.
- **CRUD -> REST Method Matches:** Crud is CREATE READ UPDATE DELETE -> REST: GET POST PUT DELETE
- **Mock Testing:** A method in jest used to test methods. Instead of using real life data like credit cards or make network requests. It fake data to be able to test certain methods.

#### When should you use JSON Web Tokens?

- **Authorization:** This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

- **Information Exchange:** JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

- What is the JSON Web Token structure?

  1. Header : The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
  1. Payload : The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. 
  1. Signature :  can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.

