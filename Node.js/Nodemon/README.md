# Nodemon
Nodeemon is one of those handy tools for working with Node.js. Basically it is a file watcher that internally runs the node command itself.


## Settings 

### Step 01
Create in "package.json"
```bash
# custom script to start nodemon
script: "dev": "nodemon src/server.js"
# start nodemon with the script
yarn dev
```


### Step 02 (this step is necessary to run nodemon with sucrase) 
Create nodemon.json file and add "script.txt" 
* [script.txt](https://github.com/AlvaroYmagawa/GoStack08/blob/master/Node.js/Nodemon/script.txt)
	
