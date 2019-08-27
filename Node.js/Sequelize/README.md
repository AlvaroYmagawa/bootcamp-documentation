# Settings 01
	This setting is required to inform file paths for sequelize.

## Step 01
	Create .sequelizerc file

## Step 02
	Change the sintaxe file to JavaScript

## Step 03
	Add "script.txt" inside the file


# Settings 02
	This setting has the db informations, see the structure int "databaseSample.txt"
	To see more acess https://sequelize.org/master/manual/dialects.html#postgresql
	
## Step 01 
	Create a database.js file

## Step 02
	Settings the information of your Db 

# How to create a table in db

## Step 01
	yarn sequelize migration:create --name"name-table" - create the table file

## Step 02
	Edit the table file and create the atributes of the table see the structure in the "tableExample.txt"

## Step 03
	yarn sequelize db:migrate - create the table in db


