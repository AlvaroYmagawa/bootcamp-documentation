# Nodemailer

Nodemailer its a package to handle with email sending.

## Instalation

    yarn add nodemailer

## Mail services

- Amazon SES
- Mailgun
- Mandril(Just with MailChimp)
- Mailtrap(Only for development)

## How to send a mail

### Step 01

First create a new file in config folder called "mail.js".

- [mail.js](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/main.js.txt)

### Step 02

Set the file with the mailtrap settings.

- Acess this link to get the mailtrap settings: https://mailtrap.io

### Step 03

Create a new folder inside the src called "lib" (lib usually used for storage external controls)

### Step 04

Inside the lib folde create a "Mail.js" model.

- [Mail.js](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/modelExample.txt)

### Step 05

Import Mail model to some controller and add the send email method.

- [Send mail example](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemailer/sendMailExample.txt)

## Templates Enginee

Templates enginee are used to personalizete your email with html and css sintaxe, and the templates can read JavaScript variables.

- See more here: [Handlebars](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Handlebars)
