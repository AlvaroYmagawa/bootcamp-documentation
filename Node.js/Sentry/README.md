# Sentry
Sentry is a error handling tool.

## Installation

### Step 01
To install sentry firt you need to create a project in your sentry account
* https://sentry.io

### Step 02
Install the sentry packege, you will find a sintaxe in sentry installation steps.

### Step 03
Create a "sentry.js" config file inside the "config" folder.
* [sentry.js](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Sentry/sentry.js.txt)

### Step 04
Import this configs and Sentry in your "app.js".
```bash
import * as Sentry from '@sentry/node';
import sentryConfig from './config/sentry';
```
Then add this sintaxe before the routes.
	 this.server.use(Sentry.Handlers.requestHandler());
And add this sintaxe after routes.
this.server.use(Sentry.Handlers.errorHandler());

### Step 05
Add this in your "app.js" constructor to active the Sentry.
	Sentry.init(sentryConfig);

### Step 06
Install the express async errors handler. This package is nedded to deal with async functions and catch they errors.
* Import this sintaxe in your "app.js" need to be imported before the routes.
	yarn add express-async-errors

### Step 07
Create a exceptionHandler() middleware to catch errors and return then in JSON format, and call in the constructor().
[exceptionHander()](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Sentry/middlewareError.txt)

