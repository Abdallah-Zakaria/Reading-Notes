# Event Driven Applications

#### Why is access control important?
Minimize the risk of unauthorized access to physical and logical systems and ensures security technology and access control policies are in place to protect confidential information.

#### Describe an application that would need access control.
Social media platforms like facebook that need to check if the user its normal user or he have a business page

#### What is a role used for?
To make the server know what this user allowed to access
#### Why is role based access control more scalable than discretionary or mandatory access control?
Role-based access control (RBAC), also known as role-based security, is a mechanism that restricts system access. 
It involves setting permissions and privileges to enable access to authorized users. Most large organizations use role-based access control to provide their employees with varying levels of access based on their roles and responsibilities. This protects sensitive data and ensures employees can only access information and perform actions they need to do their jobs.

An organization assigns a role-based access control role to every employee; the role determines which permissions the system grants to the user. For example, you can designate whether a user is an administrator, a specialist, or an end-user, and limit access to specific resources or tasks. An organization may let some individuals create or modify files while providing others with viewing permission only.

## Event-Driven Programming in Node.js
Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. In this article we’re going to go over how Event-Driven Programming works and how we can make the best use of it in our Node.js projects.

Most developers are introduced to concepts of Event-Driven Programming early on in their study of programming yet they might not fully realize it until a bit later. You’ll find that the concept is rather ubiquitous. Check any major framework or software out there and odds are you’ll find evidence of Event-Driven Programming.

## Node.js v15.0.1 Documentation Event 
* Event: 'removeListener'
* Event: 'newListener'
* EventEmitter.listenerCount(emitter, eventName)
* EventEmitter.defaultMaxListeners
* EventEmitter.errorMonitor
* emitter.addListener(eventName, listener)
* emitter.emit(eventName[, ...args])
* emitter.eventNames()
* emitter.getMaxListeners()
* emitter.listenerCount(eventName)
* emitter.listeners(eventName)
* emitter.off(eventName, listener)
* emitter.on(eventName, listener)
* emitter.once(eventName, listener)
* emitter.prependListener(eventName, listener)
* emitter.prependOnceListener(eventName, listener)
* emitter.removeAllListeners([eventName])
* emitter.removeListener(eventName, listener)
* emitter.setMaxListeners(n)
* emitter.rawListeners(eventName)
* emitter[Symbol.for('nodejs.rejection')](err, eventName[, ...args])
* event.bubbles
* event.cancelBubble()
* event.cancelable
* event.composed
* event.composedPath()
* event.currentTarget
* event.defaultPrevented
* event.eventPhase
* event.isTrusted
* event.preventDefault()
* event.returnValue
* event.srcElement
* event.stopImmediatePropagation()
* event.stopPropagation()
* event.target
* event.timeStamp
* event.type
