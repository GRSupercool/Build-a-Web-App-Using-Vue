# WATS 4000 - Example Vue.js App for Testing

> An example project for testing development environments.

This project asks you to set up your development environment, and then clone
this repository. Once you've cloned the repository, you will need to complete
the "Build Setup" below, and then you can run the development version of the
site on your local machine.

The goal here is to test your development environment to make sure it works
properly for the more complex work we will be doing later, and to start getting
an idea of what files and parts are included when we use `Vue-CLI` to
bootstrap a new project skeleton.

## Before You Begin

Be sure to set up your local development environment first. You can follow the
guidance in [Practical JavaScript 2: Building Applications](https://suwebdev.github.io/WATS-4000-gitbook/setting-up-workspace/) to get
started. Don't hesitate to supplement that resource with others specific to your
platform.

In order to run this project you will need an environment with the following:

* Working installation of Node.js
* Working installation of Git SCM
* Working setup for your Github account

## Basic Requirements
In order to successfully complete this project, fulfill the following
requirements.

* Set up your local development environment.
* Fork this repository into your own Github account.
* Clone this repository to your working development environment.
* Install dependencies by running `npm install` in the root of the repository.
* Test the site by running `npm run serve` to start the development server.
* Read through the site code and note the following:
   
   
   * What directories do you see? How do you interpret their names?
  App running at:
  - Local:   http://localhost:8080
  - Network: http://192.168.9.75:8080
  The directories are most liely the location of the  front and backend server addresses and locations.
 
 
 
    * Where is the Vue app defined? (Which file?)
    The Vue app is defined in the  vue.config.js file
    
    
    *What is listed in `package.json`?
    
    "name": "up-and-running",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
  "dependencies": {
    "vue": "^2.5.21"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "^3.3.0",
    "@vue/cli-plugin-eslint": "^3.3.0",
    "@vue/cli-service": "^3.5.3",
    "babel-eslint": "^10.0.1",
    "eslint": "^5.8.0",
    "eslint-plugin-vue": "^5.0.0",
    "vue-template-compiler": "^2.5.21"
  },
  "eslintConfig": {
    "root": true,
    "env": {
      "node": true
    },
    "extends": [
      "plugin:vue/essential",
      "eslint:recommended"
    ],
    "rules": {},
    "parserOptions": {
      "parser": "babel-eslint"
    }
  },
  "postcss": {
    "plugins": {
      "autoprefixer": {}
    }
  },
  "browserslist": [
    "> 1%",
    "last 2 versions",
    "not ie <= 8"
  ]
}

    
    
  
    
* Press `ctrl-c` in the terminal to exit the development server.


* Run `npm run build` and take a look at both the webpage that comes up and the output in the console. 

Consider the following questions:
    * what is in the node_modules directory?
   The  node modules directory  has  an abundance of files including webpack files. 
    
    
    * where can you find the directions for the scripts run with `npm run`, that is the `serve` and `build` scripts 
    Scripts available in up-and-running via `npm run-script`:
  serve
    vue-cli-service serve
  build
    vue-cli-service build
  lint
    vue-cli-service lint
    
    * what's the difference between the `dependencies` and `devDependencies` object in the package.json file?
   The Dependcies and Devdependies vary  based on the number of plugins, vue/cli files, templates, and versions of vue files. 
   
   "dependencies": {
    "vue": "^2.5.21"
    
    
    "devDependencies": {
    "@vue/cli-plugin-babel": "^3.3.0",
    "@vue/cli-plugin-eslint": "^3.3.0",
    "@vue/cli-service": "^3.5.3",
    "babel-eslint": "^10.0.1",
    "eslint": "^5.8.0",
    "eslint-plugin-vue": "^5.0.0",
    "vue-template-compiler": "^2.5.21"
    
    * Explore the `docs` directory. What do you see?
    
    The docs file has  the assets for the repository. The index.html, .gitkeep, and assets folder including the static files, css, js files.
    
    
    
    
    * Do you see the filenames of the static files? What seems odd about those filenames?
    
    The static files names have the prefix app. and suffix .map.
    
    
    
    
    * Do you see the contents of your JS and CSS files? What has happened to those contents?
     They've been optimized for app usage, include vue and webpack files for front end functionality,andthe  functionality most likely built by a 3rd party. 
    
    
    * Three config files have been supplied for you: `vue.config.js`, `aliases.config.js` and `.babel.config.js`. What is the general purpose of each file.  
    
  
   
   
   The.babel.config.js file  "which is the JavaScript ES Transpiler. This allows you to invoke state of the art JavaScript features". Accordng to scotch.io  Transpilers, or source-to-source compilers, are tools that read source code written in one programming language, and produce the equivalent code in another language. Aliases files are shortcutfiles functionality export with differnt export names, and the vue.config files are optional config file that will be automatically loaded by @vue/cli-service if it's present project root (next to package.json). You can also use the vue field in package.json, but do note in that case you will be limited to JSON-compatible values only. all the config files help make our code browser compatible.
   
   
    * Describe (in words and with a flowchart/diagram) what happens when the `npm run build` command is executed to the best of your ability.  
    Allows  me to add code, webpack,and files from someone elses  library. Adding the additional settings, files, minification and configurations to build to build and deply an app. 
    
    
    * Make a diagram of the components of this system like the ones shown in the Practical JavaScript 2: Building Applications book `Types of Website Architectures`. Do your best to document your interpretation of the architecture of this system.
    
* Deploy your code to github.com and set up gh-pages on the `docs` directory.



## Stretch Goals
If you crave a challenge, attempt some of these goals.

* Modify some of the styles to present a nicer-looking app.
* Add a message that is populated with data from the Vue component (and output it into the template).
* Do some other fiddling with the logic to experiment and learn.

## Build Setup
The following commands will help you work with this project.

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run serve

# build for production with minification
npm run build

```

For detailed explanation on how Vue works, check out the [guide](https://cli.vuejs.org/guide/) and [docs for vue-loader](https://cli.vuejs.org/config/#css-loaderoptions).
