# Application State with Redux

#### What are the advantages of storing tokens in “Cookies” vs “Local Storage”
Cookies are read server-side, and local storage is read client-side, so if the server needs the data, then it is better to use cookies.

#### Explain 3rd party cookies.
tracked by websites other than the one you are currently visiting.

#### How do pixel tags work?
Is a single transparent pixel added to a web page.


**cookies**	These are small files on a user's computer that hold data specific to a client and a website, which allow a webpage to be catered to a specific user.
**authorization**	Authorized the user to go to different areas based on what they are allowed to see and do.
**access control**	This restricts access to different areas of a network based on a person's role in an organization.
**conditional rendering** Check some logic before render the user certain components.

#### What is Redux?#
It helps to understand what this "Redux" thing is in the first place. What does it do? What problems does it help me solve? Why would I want to use it?

Redux is a pattern and library for managing and updating application state, using events called "actions". It serves as a centralized store for state that needs to be used across your entire application, with rules ensuring that the state can only be updated in a predictable fashion.

#### Why Should I Use Redux?#
Redux helps you manage "global" state - state that is needed across many parts of your application.

The patterns and tools provided by Redux make it easier to understand when, where, why, and how the state in your application is being updated, and how your application logic will behave when those changes occur. Redux guides you towards writing code that is predictable and testable, which helps give you confidence that your application will work as expected.

#### When Should I Use Redux?#
Redux helps you deal with shared state management, but like any tool, it has tradeoffs. There are more concepts to learn, and more code to write. It also adds some indirection to your code, and asks you to follow certain restrictions. It's a trade-off between short term and long term productivity.

#### Redux is more useful when:

You have large amounts of application state that are needed in many places in the app
The app state is updated frequently over time
The logic to update that state may be complex
The app has a medium or large-sized codebase, and might be worked on by many people

