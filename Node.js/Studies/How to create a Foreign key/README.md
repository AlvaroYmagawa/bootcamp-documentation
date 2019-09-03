# How to references a foreign key

## Step 01
You'll need to create a new migration 
	yarn sequelize migration:create --name"suggestive-name"

## Step 02
Now inside the new migration set the foreign key.
* [New migrate example](https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/newMigrate.txt)

## Step 03
Create the new foreign key
	yarn sequelize db:migrate

## Step 04
We still need to relacionate models so create a new static method in the class that will receive the foreign key
* [Static method example](https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/newMethod.txt)

## Step 05
Now call the method in connection db file "index.js"
* [Call method example](https://github.com/AlvaroYmagawa/GoStack8/blob/master/Node.js/Sequelize/callMethod.txt)
