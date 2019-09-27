# Node.js

- Node is a platform for backend development.
- Does not handle end user events
- Use routes and integrations
- Built on top of the V8 (Google Chrome Enginne).
- Comparable:
  - PHP
  - Ruby
  - Python
  - Go;

## Node.js advantages

- ### Event-loop architecture

  Node has the event loop architecture that constantly monitors event triggers. When a event is triggered Node send them to the "Call Stack".

  - #### Call Stack
    Call stack is a stack of events, whenever an event is triggered the node puts it in the call stack and executes in stack form.

- ### Single-Thread

  Node runs on only one thread of our processor, but since node uses many C ++ libs, we have "libuv" that allows the use of multithreads "behind the scenes", increasing the performance of responses to the client.

- ### Non-Blocking I/O

  Does not block client connection after response is provided, making real-time applications like chats.

## NPM & YARN

- Package managers
- We can use third party libraries
- Constantly updated
- Comparable:
  - PHP composer;
  - Gems
  - Python PIP

## Packages

- [Express](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Express) : Server creation.

- [Nodemon](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Nodemon) : Restart the server automatically after save.

- [Eslint](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Eslint) : Code standardization.

- [Prettier](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Prettier) : Beautify your code.

- [EditoConfig](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Bee-Queue) : Export your code standardization settings.

- [JWT (Json Web Token)](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Jwt) : User authentication package

- [Yup](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Bee-Queue) : Field validation package

- [Bscryptjs](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Bscryptjs) : Package to encrypt data

- [Sequelize](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Sequelize) : Object Relational Mapper (ORM), uses JS syntax to manipulate databases

- [Date-fns](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Date-fns) : A package for data-type variable manipulate.

- [Mongoose](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Mongoose) : Object Relational Mapper (ORM) for MongoDb.

- [Multer](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Multer) : Library to support multplataform data, supports physical files like images

- [Nodemailer](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Nodemailer) : A package to deal with mail sending.

- [Bee-Queue](https://github.com/AlvaroYmagawa/GoStack08/tree/master/Node.js/Bee-Queue) : A simple, fast, robust job/task queue for Node.js, backed by Redis.
  Redis is a performed database.

## Tools

- [Yarn](https://yarnpkg.com) : Package manager

- [Insominia](https://insomnia.rest/download/) : Tool for debugging and handling url requests

- [PostBird](https://electronjs.org/apps/postbird) : database interface for postgres

- [Docker](https://docs.docker.com/install/) : Tool for create container that isolate the data inside the container

- [MongoDB Compass](https://www.mongodb.com/download-center/compass) : database interface for mongoDb.

- [Sentry](https://sentry.io) : error handling tool
