# Advanced Mongo/Mongoose
#### Why would a developer choose to make data models?
To have a overview on his structure schema and the collections 
#### What purpose do CRUD operations serve?
There is a four function used in crud applications that linked with databases (create , read , update and delete), it's allow to create new row in the database and access to fetch data from database or update some rows and delete.
#### What kind of database is Postgres? What kind of database is MongoDB?
- Postgres is a SQL database relational databases
- MongoDB is a NoSQL database not a relational databases.
#### What is Mongoose and why do we need it?
Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

## Document the following Vocabulary Terms.
- **database:** A data structure that stores organized information
- **data model:** An abstract model that organizes elements of data and standardizes how they relate to one another and ot hte properties of real-world entities
- **CRUD:**Short for Create, Read, Update and Delete - the four basic functions that models should be able to do at a bare minimum.
- **schema:** The skeleton structure that represents the logical view of the entire database - defining how data is organized and how the relations among them are associated
- **sanitize:**To remove illegal characters from data, for the purpose of protection from malicious data	
- **SQL:** A language that allows one to write database queries. These databases use a schema and store data in tables
- **NoSQL:** A NoSQL database is exactly the type of database that can handle the sort of unstructured, messy and unpredictable data that our system of engagement requires.
- **MongoDB:** MongoDB is an object-oriented, simple, dynamic, and scalable NoSQL database. It is based on the NoSQL document store model. 
- **Mongoose:** An ODM library for MongoDB and Node.js which manages relationships between data, provides schema validation
- **record:** The data in the collections
- **document:** Document is the container of the data inside the collections
- **Object Relation Mapping (ORM):**A programming technique in which a metadata descriptor is used to connect object code to a relational database

## In-memory database pros & cons
**Pros:**

- No need for mocks: Your code is directly executed using the in-memory database, exactly the same as using your regular database.
- Faster development: Given that I don't need to build a mock for every operation and outcome but only test the query, I found the development process to be faster and more straightforward.
- More reliable tests: You're testing the actual code that will be executed on production, instead of some mock that might be incorrect, incomplete or outdated.
- Tests are easier to build: I'm not an expert in unit testing and the fact that I only need to seed the database and execute the code that I need to test made the whole process a lot easier to me.

**Cons:**

- The in-memory database probably needs seeding
More memory usage.
- Tests take longer to run (depending on your hardware).

#### conclusion
he in memory database turned out to be perfect to test applications where the logic is mainly handled through database operations and where the memory and execution time are not an issue.