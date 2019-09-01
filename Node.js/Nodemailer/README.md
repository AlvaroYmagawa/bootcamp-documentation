# Nodemailer
Nodemailer its a package to handle with email sending.

## Instalation
	yarn add nodemailer

## How to send a mail

### Step 01
First create a new file in config folder called "mail.js".
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/main.js.txt

### Step 02
Set the file with the mailtrap settings.
* Acess this link to get the mailtrap settings: https://mailtrap.io

### Step 03
Create a new folder inside the src called "lib" (lib usually used for storage external controls)

### Step 04
Inside the lib folde create a "Mail.js"model.
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/modelExample.txt

### Step 05
Import Mail model to some controller and add the send email method.
* Example: https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/sendMailExample.txt


## How to create a mail template enginees.
Templates are used to standardize your mails. You can use html and css elements on this templates to customize them and receive node variables to make it dynamic.

### Step 01
You'll need 2 packages to use the templates.
```bash
# install express-handlebars integration
yarn add express-handlebars
# install nodemailer-express-handlebars integration
yarn add nodemailer-express-handlebars
```


