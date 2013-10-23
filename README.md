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
  See the [Config File](./_configuration.scss), which should be pretty much self-explaining.
  Basically the names of the icon-styles are matched together with the index the according icons
  have in the font.

## Quick Install
  * Open your Unix-Shell and change into the directory you want the project
  to be cloned to and then clone the project to your local drive:

    $ git clone https://github.com/FloNeu/sass-icon-font-importer.git

  * Open the sass-file you want the mixings imported to and include
  the icon-font importers main-file.

    `@import "./path/to/mixingd/sass-icon-font-importer/iconFontImport";`

  * Then use this scss-snippet to call the mixing to create the the css needed for using
    the icon-fonts, according to your configuration.

    ```
    // Imports only foundation social icon-font
    $icon-fonts-to-import: (
        "social"
        , "general"
        , "general-enclosed"
        , "accessability"
    );
    @include foundation-icon-font-importer( 
      $icon-fonts-to-import // Collection of font-keys to import
      , "true" // Enables IE7 support, "false" is default and disables IE7 support
    );
  ```
  remove unused font-identifiers from $icon-fonts-to-import collection and the according
  css will not be generated at compile time.

  * This will create all css needed to use the configured icon-font in a similar manner as seen
    on [Zurb Foundation Playground](http://zurb.com/playground/foundation-icon-fonts-3).

## Further usage
  * Edit the mixings configuration-file to make it fit your needs, and link to the 
    font-files located in the original repository-folder.

## License
[MIT License (MIT)](http://opensource.org/licenses/MIT)
Copyright (c) 2013 Florian Neumann