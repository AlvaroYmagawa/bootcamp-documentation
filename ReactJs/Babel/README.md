# Babel
Babel is a free and open source JavaScript compiler that is mainly used to convert ECMAScript 2015+ code to a backward compatible version of JavaScript that can be executed by older JavaScript engines.

## Installation
```bash
yarn add @babel/core @babel/preset-env @babel/preset-react
```

## Settings 01
This settings is required to transform a react and ES5+ sintaxe to a sintaxe that the browser understand.

### Step 01
Create a "babel.config.js" file.
[babel.config.js](https://github.com/AlvaroYmagawa/GoStack08/React/babel.config.js.txt)


## Settings 02
This settings is required to run a class with-out class constructor.

```bash
@babel/plugin-proposal-class-properties
```
### Step 02
inside babel.config.js add this: 
```bash
plugins: [
    '@babel/plugin-proposal-class-properties'
]
```
