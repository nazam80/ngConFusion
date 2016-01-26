# ngConFusion
Project for Front-End JavaScript Frameworks: AngularJS course. 
The purpose of this project is to learn angularjs.

## Setup
- You should have installed node, npm and bower on your computer. To be sure, you can type in a terminal:
``` bash
    node -v
    npm -v
    bower install
```
- Open a terminal window and go to the conFusion folder. Then at the prompt type:
    
``` bash
    bower install
```
## Installing Grunt
- At the command prompt, type the following to install Grunt command-line interface (CLI):
``` bash
     npm install -g grunt-cli
```
- Next install Grunt to use within your project. To do this, go to the conFusion folder and type the following at the prompt:
``` bash     
     npm install grunt --save-dev
```
- Next, we are going to set up our first Grunt task. The JSHint task validates our JavaScript code and points out errors and gives warnings about minor violations. To do this, you need to include some Grunt modules that help us with the tasks. Install the following modules by typing the following at the prompt:
``` bash
     npm install grunt-contrib-jshint --save-dev
     npm install jshint-stylish --save-dev
     npm install time-grunt --save-dev
     npm install jit-grunt --save-dev
```     
- Next you will install the Grunt modules to copy over files to a distribution folder named dist, and clean up the dist folder when needed. To do this, install the following Grunt modules:
``` bash
     npm install grunt-contrib-copy --save-dev
     npm install grunt-contrib-clean --save-dev
```
- We are now going to use the Grunt usemin module together with concat, cssmin, uglify and filerev to prepare the distribution folder. To do this, install the following Grunt modules:
``` bash
     npm install grunt-contrib-concat --save-dev
     npm install grunt-contrib-cssmin --save-dev
     npm install grunt-contrib-uglify --save-dev
     npm install grunt-filerev --save-dev
     npm install grunt-usemin --save-dev
```     
- The final step is to use the Grunt modules watch, connect and watch, to spin up a web server and keep a watch on the files and automatically reload the browser when any of the watched files are updated. To do this, install the following grunt modules:
``` bash
     npm install grunt-contrib-watch --save-dev
     npm install grunt-contrib-connect --save-dev
```       
- Now if you type the following at the command prompt, it will build the project, and open the web page in your default browser. It will also keep a watch on the files in the app folder, and if you update any of them, it will rebuild the project and load the updated page into the browser (livereload)
``` bash
     grunt serve
```