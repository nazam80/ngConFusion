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
- Next install Grunt to use within your project. To do this, go to the ngConFusion folder and type the following at the prompt:
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
- You need to create a Grunt file containing the configuration for all the tasks to be run when you use Grunt. We have a file named Gruntfile.js in the ngConFusion folder. Also, we need a file named .jshintrc for module jsHint.
- You can run the grunt task by typing the following at the prompt:
``` bash
     grunt
```     
- Now if you type the following at the command prompt, it will build the project, and open the web page in your default browser. It will also keep a watch on the files in the app folder, and if you update any of them, it will rebuild the project and load the updated page into the browser (livereload)
``` bash
     grunt serve
```

## Web Tools: Gulp
In previous exercise we installed Grunt to learn how to use it as task runner. In next exercises, we are going to use Gulp, another task runner.
If you have follow the history coding you should do the next task before install Gulp:
- Go to the node_modules folder in conFusion, and delete all the folders/files there. We will not be using the Grunt modules anymore.
- Restore the package.json file with the initial content.
### Installing Gulp
- At the command prompt, type the following to install Gulp command-line interface (CLI) globally:
``` bash
     npm install -g gulp
```     
This will install the Gulp globally so that you can use it in all projects.
- Next install Gulp to use within your project. To do this, go to the ngConFusion folder and type the following at the prompt:
``` bash
     npm install gulp --save-dev
```
This will install local per-project Gulp to use within your project.
- Install all the Gulp plugins that you will need for this exercise. To do this, type the following at the command prompt:
``` bash
npm install jshint gulp-jshint jshint-stylish gulp-imagemin gulp-concat 
gulp-uglify gulp-cssnano gulp-usemin gulp-cache gulp-changed gulp-rev 
gulp-rename gulp-notify  browser-sync del --save-dev
```
I had a lot of problems installing these packages in MS Windows 7 due to node-gyp dependency. If you have any error installing them, follow instuctions in https://github.com/nodejs/node-gyp 
- Similarly to grunt, you need to create a Gulp file containing the tasks to be run when you use Gulp. We have a file named gulpfile.js in the ngConFusion folder.
- At the command prompt, if you type gulp it will run the default task:
``` bash
     gulp
```     
- We configured the BrowserSync and the Watch tasks in the Gulp file. To use them, type the following at the command prompt:
``` bash
     gulp watch
```
## Angular Scope

- Since Angular involves writing a lot of JavaScript, once we introduce the $scope, we need to make sure that when the uglify task runs, it does not end up mangling the $scope. Otherwise the JavaScript code will not work. Fortunately, we have an gulp plugin named gulp-ng-annotate, which ensures the mangling does not cause any problems. We now need to add this plugin and update the gulpfile.js to include this plugin.
- Install the gulp-ng-annotate plugin:
``` bash
     npm install gulp-ng-annotate --save-dev
```
## Installing Angular UI-Router

- Use Bower to install angular-ui-router by typing the following at the command prompt:
``` bash
     bower install angular-ui-router -S
```     