# Sequelize
Sequelize is an Object-Relational Mapper (ORM) for Node.js. ... It allows you to create, search, change and remove database data using JS objects and methods, as well as make changes to the table structure. It supports PostgreSQL, MySQL, MSSQL and SQLite databases.

## Setting 01
This setting is required to inform file paths for sequelize.

### Step 01
Create ".sequelizerc" file

### Step 02
Change the sintaxe file to "JavaScript"

### Step 03
Add https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/script.txt inside the file


## Setting 02
This setting has the db informations.
	
### Step 01 
Create a "database.js" file

### Step 02
Settings the information of your Db , see the structure in:
https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/databaseSample.txt



## How to create a table in db

### Step 01
	yarn sequelize migration:create --name"name-table" - create the table file

### Step 02
	Edit the table file and create the atributes of the table see the structure in the "tableExample.txt"

### Step 03
	yarn sequelize db:migrate - create the table in db


## How to connect with db

### Step 01
Create a new .js file

### Step 02
Setting the structure like this file:
https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/connectDb.txt 

### Step 03
import the file inside app 



## Sequelize Dialects
For each database you'll need a package to install, here you can see the packages:
https://sequelize.org/master/manual/dialects


