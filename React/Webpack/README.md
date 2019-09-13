# Webpack
It's a wrapper module, mainly for JavaScript.



## Installation
```bash
yarn add webpack webpack-cli
```



## Settings 01
This settings is required to set the file that will be converted by the babel loader into a bundle.js file.

### Step 01
Create a webpack.config.js file
[webpack.config.js](https://github.com/AlvaroYmagawa/GoStack08/React/Webpack/webpack.config.js.txt))
```bash
# install babel loader
yarn add babel-loader
```

### Step 02
Create a scripts to run webpack.
```bash
"scripts": {
    "build": "webpack --mode development"
  },
```

### Step 03
Now create a index.html in public folder and add the bundle.js inside a <script src"">



## Settings 02
This settings is required to run webpack server.

### Step 01
```
# install the service to run automatic
yarn add webpack-dev-server -D
```

### Step 02
Now inside the webpack.config.js add devServer:{}.
```
devServer: {
    contentBase: path.resolve(__dirname, 'public'), // to run index.html automatic
  },
```

### Step 03 
Now change the "build" script.
```
"scripts": {
    "build": "webpack-dev-server --mode development" 
  },
```

### Step 04
Now you can run "build" to run the webpack server and access the url that will be generated.



## Add Css and style loader 

### Step 01
First you need to install this 2 packages
```bash
yarn add css-loader style-loader -D
```
### Step 02
Now add this inside rules in "webpack.config.js"

```bash
{
  test: /\.css$/,
  use: [
    { loader: 'style-loader' },
    { loader: 'css-loader' }
  ]
}
```

### Step 03
Import in App.js your css file.
```bash
import './App.css'
```



## Add file loader

### Step 01
First you need to install this package
```bash
yarn add file-loader -D
```

### Step 02
Now add this inside rules in "webpack.config.js"
```bash
{
  test: /.*\.(gif|png|jpe?g)$/i,
  use: {
    loader: 'file-loader'
  }
}
```

### Step 03
Import in App.js your file 
```bash
import profile '.assets/profile.jpg'

<img src={profile}\> // to use inside a img
```




## Modes

### mode development // generate a readable bundle 

### mode production //Generates a lighter bundle

