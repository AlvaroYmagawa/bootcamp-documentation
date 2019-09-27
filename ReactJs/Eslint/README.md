# How to config Eslint for react

## 1. 
Install eslint in a devDependence
	yarn add eslint -D

## 2. 
Start eslint service
	yarn eslint --init

## 3. 
Answer the questions and select react.


## 4. 
Delete package.json.lock because we are using yarn and by default eslint use npm to install the packages.

## 5. 
Run yarn in your project root to update the yarn.lock.
	yarn

## 6. 
Now install prettier in a devDependence.
	yarn add prettier eslint-config-prettier eslint-plugin-prettier babel-eslint -D

## 7.
Now in your '.eslintrc.js' file you need to setting some things.
### 7.1 
	- First in 'extends' we'll extends prettier and prettier/react configurations
```bash
# Example
	extends: [
	  'airnbnb',
	  'prettier',
	  'prettier/react'
	]
```

### 7.2 
	- Before 'parseOptions' we'll create a parse element that will receive the babel-eslint.
```bash
# Example
	parser: 'babel-eslint'
```

### 7.3
	- In 'plugins' we need to add prettier.
```bash
# Example
	plugins: [
	  'react',
	  'prettier'
	]
```

### 7.4
	- Now we'll overwrite some rules that come by default.
	- rule 01: Everything not in the rules is pointed to as an error.
	'prettier/prettier': 'error'
	- rule 02: by default airbnb syntax jsx is only accepted in .jsx files so let's make it accepted in .js files too
	'react/jsx-filename-extension':[
	  'warn',
	  { extensions: ['.jsx', '.js'] }
	],
	'import/prefer-default-export': 'off' // Now you can have a file with none export default
	



