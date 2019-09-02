# Multer
Library to support multplataform data, supports physical files like images.


## Installation
```bash
# install multer
yarn add multer

```

## Settings 01
This settings is required to set the folders thas will storage the files received.

### Step 01
First you'll need to create a file to store the files that the application will receive.
* Create a tmp folder out of src folder
* Then create a uploads folder inside the tmp

### Step 02
Now you have to set the configurations in some file.
* Create a "multer.js" config file.
* [multer.js](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Multer/multerConfig.txt)

## Settings 02
This settings is required to control the route of the file request with a middleware

### Step 01
* Import multer from 'multer'in routes.js file
* Import the multerConfig 
* Create a const update thats receive multer(multerConfig)
* Insert the middleware update with this sintaxe:
	upload.single('file'),





