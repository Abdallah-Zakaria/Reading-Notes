# OAuth

####  Why is authentication important?
To protect the users and make sure each one fatch and access to his data only. 

#### Why should we be careful about storing a user’s password?
To protect sensitive information for the users if to get access and permission.

#### What is the difference between hashing and encryption?
Encrypted can be decrypted, but hashed cannot be unhashed and hashing is more secure than encryption.

#### What is the difference between encryption and encoding?
Encoding can be reversed by the same algorithm, but encryption needs a key to be reversed, so encryption is more secure than encoding.

#### What is a token used for?
Authenticate a a user.

**authentication**	Verifying a user's identity by requiring pre-required details.

**authorization**	The process of allowing a user access to a resource.

**encryption**	The translation of data to another form so that only a secret key or password can read it.

**hashing**	The conversion of one value to another. This is done to make data like passwords difficult to decipher.

**session**	Interactions with a website that take place in a given time frame.

**cookie**	A small amount of data that is stored by the web browser to so a website can remember information about you. 

**token**	With token based authentication, the user state is stored on the client. The data is encrypted in a JWT. The server then validates the JWT.

**basic Auth**	An authentication built into HTTP , where the authorization header contains the word basic followed by a space and an encoded string of username:password

**encoding**	The process of converting one code of data to another. It goes from something a user can understand to something less clear.

**secret**	This ia a secret that only the application and authorizaiton server know. It should be random enough that it can not be guessed.

**cryptography**	Protecting information by transforming it into a format that can not be easily understood.


### The Third-Party Application: "Client"
The client is the application that is attempting to get access to the user's account. It needs to get permission from the user before it can do so.

### The API: "Resource Server"
The resource server is the API server used to access the user's information.

### The Authorization Server
This is the server that presents the interface where the user approves or denies the request. In smaller implementations, this may be the same server as the API server, but larger scale deployments will often build this as a separate component.

### The User: "Resource Owner"
The resource owner is the person who is giving access to some portion of their account.

