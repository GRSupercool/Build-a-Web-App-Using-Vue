# Test Project for buiding Web Apps in Vue 
Vue.js App for Testing

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


## How to set up the development environment
## Build Setup
The following commands will help you work with this project.

``` bash
# install dependencies
npm install

## How to run the development server 
# serve with hot reload at localhost:8080
npm run serve

# build for production with minification
npm run build

```

For detailed explanation on how Vue works, check out the [guide](https://cli.vuejs.org/guide/) and [docs for vue-loader](https://cli.vuejs.org/config/#css-loaderoptions).



## How to build the code for deployment


 Install Vue-CLI
# In order to use the Vue-CLI tool, we must first install it. 
This software requires Node.js to work, and it can be installed using NPM. 
To install Vue-CLI in our development environment, run this command:

npm install -g @vue/cli
# In order to create a new app with the Vue-CLI, change directory into your Projects area and run this command:

vue create test-project

# If you're using git bash with Windows you will need to run this command to create a project:

winpty vue.cmd create test-project

# Now that we have everything installed to run our project, we can test it out by running the development server with this command:

npm run serve

# How to deploy the site.

# Configuring Deployment
To configure the deployment of our Vue.js application, we will leverage the ability of Github Pages to serve a website from the docs folder in a project repository. This means that we need to alter our configuration so that Webpack builds the code into the docs/ directory instead of the dist/ directory (which is the default location Webpack uses).

vue.config.js

To make this happen we will need to add a vue.config.js file that provides instructions for building to the docs directory. Create this file in the root of your project. The designation of publicPath: '' and outputDir: './docs/' will allow us to us deploy to a path under an account on github.io . Setting assetsDir: 'assets' means that out css and js folder will be built under the ./docs/assets directory.

Create the ./aliases.config.js

# Build the Code
In order to process our code and build the site, execute the build command:

npm run build

# When we want to deploy the code we just built, we can run the following commands:

git add docs

Then:

git commit -m "Built new version of site."

Finally:

git push origin

# Project: Deploying the App
If we have not already created a Github repository, let's do so. On github, click the big green "New" button that shows up on our profile page. This should bring you to the Create New Repository page.

# Create New Repository screen
Give the repository a name, and then select private or public. We do not need to add a README.me or any LICENSE.md files because we already have a bunch of files.

# New repository instructions
The only thing we should do different is instead of doing the command git add README.md we should add everything with git add -A

# Configuring Webpack
Once we have created our repository on Github, we must configure Webpack to build our files into the docs/ directory. This requires us to add the ./vue.config.js and ./aliases.config.js files.

# Create the two new files in the root of your project and copy the contents below into them.

vue.config.js
aliases.config.js

# After creating the config files, run the build command:

npm run build

# Configure Github Pages
In order to deploy our site to Github Pages, we must alter the settings on our repository. From the repository homepage, click "Settings".

# GitHub Pages configuration

The Source setting should be "master branch /docs folder". This will allow our users to view our project at a URL that matches the pattern https://username.github.io/project-name/. When we click "Save" next to the GitHub Pages Source setting, the Settings page will refresh and it will show you the URL where our site has been deployed.

