# Access Control (ACL)

#### When is Basic Authorization used vs. Bearer Authorization?
Basic authorization used for a read only resource, and it should only be used with HTTPS . Bearer authoriztion uses a token and is more secure for an exchange between a client and a server.
#### What does the JSON Web Token package do?
Transmitting information as a JSON object. It is can be signed with a secret, whcih certifies that the only owner of the secret is the party the signed the JWT.

#### What considerations should we make when creating and storing a SECRET?
Stored secret value in the .env file. The goal with a secret is to make sure nobody has access to it, to keep your app secure.

**encryption**	The method by which information is converted into a secret code that protects the data from being easily understood.
**token**	These are strings or JWTs that let an api know that the token bearer is authorized.
**bearer**	The bearer is the 'owner' of the token in bearer authentication. The bearer shows the token and is granted access to the resource or URL.
**secret**	This is often sent along with a client id to a resource to obtain a token. It is only known to the OAuth Client and the authorization server.
**JSON Web Token**	A method for securely transmitting JSON objects between different parties. The tokens can be transmitted as query strings, header attributes, or in the body of a POST request. JWT is popular because of teh small size.


#### What is RBAC?
RBAC is nothing more than the idea of assigning system access to users based on their role within an organization. The system needs of a given workforce are analyzed, with users grouped into roles based on common job responsibilities and system access needs. Access is then assigned to each person based strictly on their role assignment. With tight adherence to access requirements established for each role, access management becomes much easier.

#### Benefits of RBAC?
With the proper implementation of RBAC, the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.

RBAC may sound intimidating, but it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.

The data breach you prevent may be your own.

- **Access control lists (ACL)** — An ACL is a means of defining access rights by a given user or user group, to a specific object, such as a document
