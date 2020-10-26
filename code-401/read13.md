# Bearer Authorization
#### Write the following steps in the correct order:

1. Register your application to get a client_id and client_secret
1. Ask the client if they want to sign in via a third party
1. Receive authorization code
1. Receive access token
1. Make a request to the access token endpoint
1. Redirect to a third party authentication endpoint
1. Make a request to a third-party API endpoint
1. What can you do with an authorization code?
1. Use an authorization code to get an access token.
#### What can you do with an authorization code?
Temporary code that the client will exchange for an access token.
#### What can you do with an access token?
Token is gain to access to the resource.

#### What’s a benefit of using OAuth instead of your own basic authentication?
Less time for user and more credibility

#### Vocabulary Terms
Term	Definition
- **Client ID**	The client ID is a public identifier for apps. It is generally stored as a hex string. 
- **Client Secret**	The secret is only known to the application and the authorization server. It should be random and unguessable.
- **Authentication Endpoint**	An HTTP endpoint that that clients can use to identify a user or obtain an authorization code that can be used to exchange for an access token.
Access Token Endpoint	This is where the app makes a request to get the access token for a user.
- **API Endpoint**	This is one end of a communication channel with an API. This is the location where an API can get the resources it needs to carry out a function.
- **Authorization Code**	After the user returns to the client on the redirect URL path, the app gets the authorization code and can use it to get an access token.
- **Access Token**	This allows an application to access an API. The app recieves an access token after the user is authenticated and authorized.


#### What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

#### When should you use JSON Web Tokens?
- Here are some scenarios where JSON Web Tokens are useful:

**Authorization**: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

**Information Exchange**: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

#### What is the JSON Web Token structure?
In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

1. Header
1. Payload
1. Signature