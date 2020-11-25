# Login and Auth

#### Why is the Context API useful?
The Context API is useful because it can change important values for many components at once from a centralized location, without all of the values having to be passed through many layers of props.

there is no need for props using it, and it do to import values for many components that are consumer it and its wrapped between it .

#### Can a component outside of a provider get its context?
No,  it's need to be wrapped between the provider.

#### What are some common use cases for using the Context API?
Change the theme and as the pofile data for the user to be access in any where inside the components.

#### Describe “Context Hell”
Without useContext, you may need to pass or drilling props to each components in the app to be access for the componnents that will consume it.

**global state**	This is the state of the entire React application that located in the context.
***gloabl context**	This is context that affects the entire application, and it will share data to everything in the React component tree.
**provider**	The context provider accepts a value that will be passed to its children. All children components will rerender when the value changes.
***consumer***	This is a React component that subscribes to context changes in value of the Provider.



### What is Role-Based Access Control
Role-based access control (RBAC) restricts network access based on a person’s role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

What if an end-user’s job changes? You may need to manually assign their role to another user, or you can also assign roles to a role group or use a role assignment policy to add or remove members of a role group.

Some of the designations in an RBAC tool can include:

- Management role scope – it limits what objects the role group is allowed to manage.
- Management role group – you can add and remove members.
- Management role – these are the types of tasks that can be performed by a specific role group.
- Management role assignment – this links a role to a role group.