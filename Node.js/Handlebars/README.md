# Handlebars
Handlebars deal with mail template enginees, Templates enginnes are used to standardize your mails. You can use html and css elements on this templates to customize them and receive node variables to make it dynamic.


## How to create a mail template enginees.

### Step 01
You'll need 2 packages to use the templates.
```bash
# install express-handlebars integration
yarn add express-handlebars
# install nodemailer-express-handlebars integration
yarn add nodemailer-express-handlebars
```

### Step 02
Now create a folder in src called "views"
1. inside the "views" create a folder "email"
2. inside "email" create a "layout" and a "partials" folder
3. in "layout" create a file called "default.hbs" this is our default mail template
* [default.bhs](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Handlebars/default.txt)
4. in "partials" create a file called "footes.hbs" this is our mail footer
* [footer.hbs](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Handlebars/footer.txt)
5. inside "email" create a file called "cancellation", we'll use this template when a user do a cancellation.

### Step 03
Now we need to set the path to this folders. To do this we need to import this 3 things in our Mail model (/lib/Mail.js).
```bash
import nodemailerhbs from 'nodemailer-express-handlebars';
import { resolve } from 'path';
import mailConfig from '../config/mail';
import exphbs from 'express-handlebars';
```

### Step 04
1. Create a configureTemplates() method in Mail model.
2. Call the method in the costructor
* [configureTemplates()](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Handlebars/configigureTemplates.txt)

### Step 05
Now to set the templates , you need to acess the send mail method and settings somethings.
* [Call templates example](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Handlebars/callTemplates.txt)


