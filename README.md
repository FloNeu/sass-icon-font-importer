## Sass-Icon-Font-Importer
  Mixing used to import multiple icon-fonts in comfortable, 
  configurable way. In example for use-cases like on
  the foundation font-icons playground-page 
  ( http://zurb.com/playground/foundation-icons )

  Produces 

## Notes
  * Tries to solve some of the problems people are having
  ( https://groups.google.com/forum/#!topic/foundation-framework-/Jj9zfn-IQbs )
  when using the sass import files delivered by the bower-package
  from https://github.com/zurb/foundation-icons.
  * Can be used to import other icon-fonts in a similar manner

## TODOs:
  * Testing of icon classes in ie7
  * Further Documentation
  * Demo-Page


## Prerequisites
  * Node.js - Download and Install [Node.js](http://www.nodejs.org/).


## Configuration
  See the [config](./config/) folder and especially the [project.js](./config/project.js) file.

## Quick Install
  Open your Unix-Shell and change into the directory you want the project
  to be cloned to and clone project to your local drive:

    $ git clone https://github.com/ForgeTech/forge-home.git

  Install npm (server side) dependencies:

    $ npm install

  Install bower (client side) dependencies:

    $ bower install

  Start grunt development-workflow:

    $ grunt server

  This will compile all of the applications source-files, runs application in development-mode
  and opens it in a browser. In this mode auto-recompilation of project-sources,

  * [Coffee-Script as Javascript-Sources](http://coffeescript.org/) ( Currently not used! )
  * [Scss as Css-Sources](http://sass-lang.com/)
  * [Jade as HTML-Sources](http://sass-lang.com/)

  , are enabled. Also the server-application is automatically restarted if files in 
  [Server-Application Folder](./server) are changed.
    
## Root - Folder Structure
  * [Scss-Cache Folder](./.sass-cache/) - Temporary cached scss-files used for faster scss-recompilation during
    development-mode.
  * [Temporary Folder](./.tmp/) - All temporary files compiled from project-sources during 
    development-mode.
  * [Frontend-Application Folder](./app/) - All files which are needed for the frontend-application.
  * [Bower-Modules Folder](./bower_modules/) - All client-side javascript-dependencies installed via bower.
  * [Configuration Folder](./config/) - Configuration files shared between frontend- and server-application.
  * [Data Folder](./data/) - Contains files for initial application-data used in development-, testing- or live
    -enviroments.
  * [Node-Modules Folder](./node_modules/) - All server-side javascript-dependencies installed via npm.
  * [Server-Application Folder](./server/) - All files which are needed for the server-application.
  * [Testing Folder](./test/) - All files needed for testing the frontend-/server-application.

## Frontend-Application - Folder Structue.
  * [Assets Folder](./app/assets/) - Folder to contain frontend-application assets like images, audio and video.
  * [Fonts](./fonts/) - Folder to contain custom web-font files used in the frontend-application.
  * [Scripts Folder](./app/scripts/) - Containing all javascript-files of the frontend-application.
    * [AngularJS-Controllers Folder](./app/scripts/controllers/) - AngularJS controllers used to provide functionallity for
      AngularJS views.
    * [AngularJS-Directives Folder](./app/scripts/directives/) - AngularJS custom frontend-application directives used in
      frontend-application.
    * [AngularJS-Filters Folder](./app/scripts/filters) - AngularJS custom frontend-application filters used in frontend-
      application.
    * [Frontend-Services Folder](./app/scripts/services/) - AngularJS services connecting the frontend-application with
      server-application CRUD-Api.
    * [Frontend-Application File](./app/scripts/app.js) - File for initialization of the frontend-application.
    * [Frontend-Routes File](./app/scripts/routes.js) - Defines the routes of the angular frontend-application.
  * [Styles Folder](./app/styles/) - Containing all frontend-application css source-files.
    * [Components Folder](./app/styles/components/) - Folder to contain scss-components used by the frontend-application
      styles.
    * [Mixing Folder](./app/styles/mixings/) - Folder to contain custom scss-mixings to be used in frontend-application
      styles.
    * [Views Folder](./app/styles/views/) - Folder to contain scss style-files directly related to frontend-application
      views
    * [Angular-Styles File](./app/styles/_angular.scss) - Contains definitions for the styles automatically applied to
      forms controlled by AngularJs.
    * [Foundation-Settings File](./app/styles/_settings.scss) - File to override the standard settings of the foundation
      -framework styles.
    * [App-Styles File](./app/styles/app.scss) - Main Style-File including/importing and configuring all of 
      frontend-applications styles
  * [Views Folder](./app/views/) - Folder to contain all views precompiled for the use in the AngularJS frontend-application 

## Server-Application - Folder Structure
  * [Configuration Folder](./server/config/) - Containing configuration files used by the server-application
  * [Controllers Folder](./server/controllers/) - Containing controllers providing functionallity for the server-application.
  * [Models Folder](./server/models/) - Defining the data-models used for setting up the server-application database.
  * [Views Folder](./server/routes.js) - Contains the jade views, layouts and partials served directly from the server in live-
  enviroment ( Are also precompiled in development-enviroment ).
  * [Server File](./server/server.js) - The main-file of the server-application importing and including all modules related to the server-application.

## License
[Creative Commons Attribution-NonCommercial-NoDerivs 2.0](http://creativecommons.org/licenses/by-sa/3.0/)
[Legal Code](http://creativecommons.org/licenses/by-sa/3.0/legalcode)
