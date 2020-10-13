# Data Modeling & NoSQL
### Name 3 advantages to Test Driven Development
1. get a overview of what to do.
1. Reduces time spent on rework.
1. Spend less time in the debugger.

### In what case would you need to use beforeEach() or afterEach() in a test suite?
For example, let's say that several tests interact with a database of cities. You have a method initializeCityDatabase() that must be called before each of these tests, and a method clearCityDatabase() that must be called after each of these tests.

### What is one downside of Test Driven Development ?
- Focusing on the simplest design now and not thinking ahead can mean major refactoring requirements.
- It’s difficult to write good tests that cover the essentials and avoid the superfluous.

### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
Difference between ES6 Classes and Constructor/Prototype Classes of the way of inheritance, prototype is itself an object instance where the class defines a type which can be instantiated at runtime.

### Name a use case for a static method
Static methods are used to implement functions that belong to the class, but it's a particular of the object.

### Write an example of a Higher Order function and describe the use case it solves
Higher-order functions are functions that take other functions as arguments or return functions as their results.
```
const array = [1,2,"x',3]
array.filter(item=>{
  return typeof(item) != Number
})
// output [1,2,3]
```

### Document the following Vocabulary Terms
- **functional programming :** is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects.
- **pure function :** is a function where return value is only determind by its input values, without observable side effects.
- **higher-order function:** Higher-order functions are functions that take other functions as arguments or return functions as their results.
- **immutable state:** immutable object (unchangeable object) is an object whose state cannot be modified after it is created.
- **object:** object is a collection of properties, and a property is an association between a key and a value. A property's value can be a function, in which case the property is known as a method.
- **object-oriented programming :** the basic idea of OOP is that we use objects to model real world things that we want to represent inside our programs, and/or provide a simple way to access functionality that would otherwise be hard or impossible to make use of.
- **class:** classes are a template for creating objects. They encapsulate data with code to work on that data.
- **prototype:** Prototypes are the mechanism by which JavaScript objects inherit features from one another.
- **super :** the super keyword is used to access and call functions on an object's parent. 
- **constructor:** Constructors have the same name as the class or struct, and they usually initialize the data members of the new object.
- **instance :** create a reference object by new.
- **Context :** point for the object whitin a function beign executed.
- **this :**refers to the object that will be created when the constructor or class is run
- **Test Driven Development (TDD):** s a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the code is improved so that the tests pass. This is opposed to software development that allows code to be added that is not proven to meet requirements.
- **Jest:** Javascript testing framework with a focus on simplicity.
- **Continuous Integration (CI):** A coding philosophy and set of practices that drive development teams to implement small changes as a mechanism to integrate and validate changes.
- **Unit Test:** Software testing method where individual units of source doe are tested to determine whether they are fit for use.

## Preview
#### SQL vs NoSQL: High-Level Differences
- SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.
- SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
- SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb
- For the type of data to be stored: SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

#### Basic principles of NoSQL data modeling
- Denormalization
- Aggregates
- Application Side Joins
- Atomic Aggregates