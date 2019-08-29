# Sequelize
Sequelize is an Object-Relational Mapper (ORM) for Node.js. ... It allows you to create, search, change and remove database data using JS objects and methods, as well as make changes to the table structure. It supports PostgreSQL, MySQL, MSSQL and SQLite databases.

## Setting 01
This setting is required to inform file paths for sequelize.

### Step 01
Create ".sequelizerc" file

### Step 02
Change the sintaxe file to "JavaScript"

### Step 03 
Set the paths in which sequelize will interact with your application.
* Example: 
https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Sequelize/script.txt



## Setting 02
This setting has the db informations.
	
### Step 01 
Create a "database.js" file

### Step 02
Set the informations of your Db.
* Example:
https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/databaseSample.txt



## How to create a table in db

### Step 01
	# create the table file
	yarn sequelize migration:create --name"name-table" 

### Step 02
Edit the table file and create the atributes of the table see the structure in the "tableExample.txt"

### Step 03
	# create the table in db
	yarn sequelize db:migrate 


## How to connect with db

### Step 01
Create a new .js file

### Step 02
Set the structure of your connection.
* Example:
https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/connectDb.txt 

### Step 03
import the file inside "app.js"


## How to references a foreign key

#### Step 01
You'll need to create a new migration 
	yarn sequelize migration:create --name"suggestive-name"

### Step 02
Now inside the new migration set the foreign key.
* Example:  https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/newMigrate.txt

### Step 03
Create the new foreign key
	yarn sequelize db:migrate

### Step 04
We still need to relacionate models so create a new static method in the class that will receive the foreign key
* Example: https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/newMethod.txt

### Step 05
Now call the method in connection db file "index.js"
* Example: https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/callMethod.txt
 



## Sequelize Dialects
For each database you'll need a package to install, here you can see the packages:
* Sequelize dialects link:
https://sequelize.org/master/manual/dialects


