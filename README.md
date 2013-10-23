## Sass-Icon-Font-Importer
  Mixing used to import multiple icon-fonts in comfortable, 
  configurable way. In example for use-cases like on
  the foundation font-icons playground-page. 
  ( http://zurb.com/playground/foundation-icons )

## Notes
  * Was created for importing multiple [Foundation Icon-Fonts](https://github.com/zurb/foundation-icons) and tries to solve some of the problems people are having
  ( https://groups.google.com/forum/#!topic/foundation-framework-/Jj9zfn-IQbs )
  when using the sass import files delivered by the bower-package.
  * Can be used to import other icon-fonts in a similar manner

## TODOs:
  * Testing of icon classes in ie7
  * Demo-Page

## Prerequisites
  * Foundation Icons - Download and Install from [Github](https://github.com/zurb/foundation-icons)
    or [Foundation Playground](http://zurb.com/playground/foundation-icon-fonts-3). You can also require the Package via [Bower](http://bower.io/) if you have it installed in your project.
  * (Recommended for Linux/Mac) 
    * Git - Download and Install [Git](http://git-scm.com/)
  * (Recommended for Windows)
    * Msysgit - Download and Install [Msysgit](http://msysgit.github.io/) providing Git and Unix-Shell for Windows

## Configuration
  See the [config](./config/) folder and the [Settings File](./_settings.scss).

## How to use it
* Place "sass-icon-font-importer" mixing-folder in your sass-directory.
* Import it to your projects sass-file using : 
    @import "./components/foundationIconFontImport/foundationIconFontImport";
* Edit the mixings settings-file to make it fit your needs, and link to the 
  font-files located in the original repository-folder.
* Call the mixing from your sass-file
  * without parameters all icon-fonts without IE7 support are imported. 
    Like: @include foundation-icon-font-importer();
  * The mixing takes to optional parameters, first a sass-collection defining
    the icon-fonts to import and second string "true" or "false" to include/exclude
    IE7 support.
    Like:
    // Imports only foundation social icon-font
    $foundation-icon-fonts-to-import: (
        "social"
        //, "general"
        //, "general-enclosed"
        //, "accessability"
    );
    @include foundation-icon-font-importer( 
      $foundation-icon-fonts-to-import // Collection of font-keys to import
      , "true" // Enables IE7 support, "false" is default and disables IE7 support
    );

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

## License
[Creative Commons Attribution-NonCommercial-NoDerivs 2.0](http://creativecommons.org/licenses/by-sa/3.0/)
[Legal Code](http://creativecommons.org/licenses/by-sa/3.0/legalcode)
