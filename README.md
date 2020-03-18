# Gutenberg Block Development Package
A Complete Package for Gutenberg Block Development. All necessary libraries are included here. Just need to npm installation.

## Steps are 
> Command Lines are Here

**Initialization of npm**

* npm init

**React & React DOM installation**

* npm install --save react react-dom

**Webpack and Webpack CLI installation**

* npm install -D webpack webpack-cli

**webpack.config.js file configuration(No. 1 configuration)**

```
module.exports = () => {
  var config = {
    entry: './src/editor.js',
    output: {
      filename: 'editor.js'
    }
  }
  return config;
}
```
**Package.json file edit (No. 1 config)**

```
{
  "name": "myblock",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "start": "webpack --mode=development --watch",
    "build": "webpack --mode=production"
  },
  "author": "Binsaifullah",
  "license": "ISC",
  "dependencies": {
    "react": "^16.8.6",
    "react-dom": "^16.8.6"
  },
  "devDependencies": {
    "webpack": "^4.30.0",
    "webpack-cli": "^3.3.0"
  }
}
```

_There are two modes (eg. development & production) and two nodes (eg. start & build). Watch is used to show the impact of a bit changing_

**[Babel Loader](https://github.com/babel/babel-loader) including babel/core babel-loader and babel preset Installation**

* npm install -D babel-loader @babel/core @babel/preset-env

**[Babel preset react](https://babeljs.io/docs/en/babel-preset-react) installation**

* npm install --save-dev @babel/preset-react
