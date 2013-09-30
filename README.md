# Kendo UI Mobile Tutorial Application

## Overview

This application takes the developer through the process of building a mobile web-application using Kendo UI Mobile. Each commit is a separate lesson teaching some aspects of Kendo UI Mobile.


## Prerequisites

### Git
- A good place to learn about setting up git is [here][git-github]
- Git [home][git-home] (download, documentation)

### Node.js
- Generic [installation instructions][node-generic].
- Mac DMG [here][node-mac]
- Windows download from [here][node-windows]. (You will also need [7 Zip] to unzip the node archive)
  (and don't forget to add `node.exe` to  your executable path)

## Commits / Tutorial Outline
You can clone the project by running `git clone https://github.com/kelvin-yong/kendo.git`  
This will create a folder `kendo` and download all code into that folder.

You can check out any point of the tutorial using `git checkout -f step???`. For example, to check out step04b, run `git checkout -f step04b`

To see the changes which between any two lessons use the `git diff` command. For example` git diff step04a..step04b`

## Step 1: Basics
Using Kendo UI Mobile, you will start to create a web page that looks an feel like a native mobile app. The app will be a tab application common iOS, with a navigation bar on the header and 2 tabs to switch between 2 views.

### step-1a

- Empty HTML5 page.
- You will link up the Kendo UI Mobile stylesheet and javascript files

### step-1b

- A HTML5 page with the necessary stylesheet and javascript files linked.
- You will bootstrap the application, add a mobile view, and link that up to a mobile layout.

### step-1c

- A mobile app skeleton, but it doesn't look mobile yet!
- You will add a navigation bar, a tab strip and another mobile view

### step-1d

- Result of step 1
- You are ready to move on to Step 2


## Step 2: Implementing Settings with List View
Here, you will use the list view widget in the setting screen to allow user to key in their inputs and save their settings.

### step-2a

- We have the application from end of Step 1
- You will start to implement the setting screen using a list view

### step-2b

- The setting screen now has a form with some input fields
- You will now add more input fields and make the list look like a grouped table


### step-2c

- The setting screen has all the required input fields
- You will now add a save button


### step-2d

- The save button is added and saving works
- You are now ready to move on to Step 3

## Step 3: Views and Transitions
Here, you will learn about multiple views and layouts, and how to use transitions to animate view switching.

### step-3a

- We have the application from end of Step 2
- Hide the save button when it is not in the settings screen by defining another layout

### step-3b
- The settings button now doesn't appear in the main screen. But the tab strip looks wrong
- Use another method, view events, to solve the save button problem
- First try $('#id'), next try $('.class') on the console
- Does it work?

### step-3c
- The save button is almost working
- Make the behaviour of the save button correct

### step-3d
- Now the save button is working, time to add some content
- You will add buttons to home view and learn how to handle button events
- Add a search result view and a back button in the navigation bar

### step-3e
- The navigation looks great
- Now add some transition

### step-3f
- Transition is now added
- You are now ready to move on to Step 4

## Step 4: Refactoring and Remote Views
The code from Step 3 is now looking messy. Time to clean up the code for maintainability!

### step-4a

- The application behaves exactly as Step 3e. However the code here has been cleaned up.
- You will change the behaviour of the home tab so that it will show either the home or results page as appropriate.

### step-4b

- The behaviour of home tab is now correct. When navigating from the settings tab to home tab, it will either display the home view or result view, depending on which was last displayed.
- You will now move the settings view to an external file. i.e. a remote view

Note that a remote view running on the local file system may not work on some browsers due to CORS restrictions. It has been tested to work on
- Firefox 19.0.2 [Mac]
- Safari 6.0.1 [Windows]
- iOS 5.1

Chrome will work if the option `--allow-file-access-from-files` is passed upon start up

Windows: C:\Users\XXX_USER\AppData\Local\Google\Chrome\Application\chrome.exe --allow-file-access-from-files

Mac: /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --allow-file-access-from-files &

### step-4c

- The settings page is now a remote view. 
- We will now concentrate on improving the home view.

### step-4d

- The home view now has the some input criteria to perform search
- You are now ready to move on to step 5

## Step 5: Datasource and Templates
In this step, we will be using datasource and templates. We will also touch on some additional widgets.

### step-5a

- The application now contains input fields for specifying the search criteria.
- A datasource has also been added for you.
- You will learn how to use the datasource, and create a result list view to display the data

### step-5b

- We now have a list widget linked to a remote data source and template
- You will learn how to make the play button work

### step-5c

- The play button and the action sheet now works.
- You now need to make your search dynamic.

### step-5d

- The play button and the action sheet now works.
- The file starts with transport.url modified.
- Type `dataSource.read({d:0})`, `dataSource.read({d:1})` or `dataSource.read()` in your JavaScript console and see what happens
- You now need to make your search dynamic, either using plain JavaScript (perhaps with jQuery), or MVVM.
- This is left as an exercise for you. Have fun!


## Other planned topics

- MVVM
- Recipes
  - Local Saving
  - Splash Screen
  - Template Performance: useWithBlock
- Advanced JavaScript
  - Debugging
  - Memory
  - Build Tools
 

## History

- Author: Kelvin Yong
- Version: 0.1.0
- 30 Sep 2013

[7 Zip]: http://www.7-zip.org/
[angular-seed]: https://github.com/angular/angular-seed
[DI]: http://docs.angularjs.org/#!guide.di
[directive]: http://docs.angularjs.org/#!angular.directive
[$filter]: http://docs.angularjs.org/#!angular.Array.filter
[git-home]: http://git-scm.com
[git-github]: http://help.github.com/set-up-git-redirect
[ng:repeat]: http://docs.angularjs.org/#!angular.widget.@ng:repeat
[ng:view]: http://docs.angularjs.org/#!angular.widget.ng:view
[node-mac]: http://code.google.com/p/rudix/downloads/detail?name=node-0.4.0-0.dmg&can=2&q=
[node-windows]: http://node-js.prcn.co.cc/
[node-generic]: https://github.com/joyent/node/wiki/Installation
[java]: http://www.java.com
[$resource]: http://docs.angularjs.org/#!angular.service.$resource
[$rouet]: http://docs.angularjs.org/#!angular.service.$route
[service]: http://docs.angularjs.org/#!angular.service
[$xhr]: http://docs.angularjs.org/#!angular.service.$xhr