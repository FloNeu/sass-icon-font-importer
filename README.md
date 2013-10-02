sass-foundation-icon-font-importer
==================================

Mixing used to import multiple foundation-icon-fonts in comfortable, 
configurable, none-conflicting way. In example for use-cases like on
the foundation font-icons playground-page ( http://zurb.com/playground/foundation-icons )

Tries to solve some of the problems people are having
( https://groups.google.com/forum/#!topic/foundation-framework-/Jj9zfn-IQbs )
when using the sass import files delivered by the bower-package
from https://github.com/zurb/foundation-icons. 

How to use it:
- Place "sass-foundation-icon-font-importer" mixing-folder in your sass-directory.
- Import it to your projects sass-file using : 
    @import "./components/foundationIconFontImport/foundationIconFontImport";
- Edit the mixings settings-file to make it fit your needs, and link to the 
  font-files located in the original repository-folder.
- Call the mixing from your sass-file
  - without parameters all icon-fonts without IE7 support are imported. 
    Like: @include foundation-icon-font-importer();
  - The mixing takes to optional parameters, first a sass-collection defining
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

Notes:
- Mainly it solves the problem with importing multiple icon-fonts,
  leading to conflicts in global namespace, caused by doublication
  of variables and mixing definitions in the sass-files
  of the original repository.
- This was my first attempt to solve a more complex problem
  using sass-scripting. So the solution may not be optimal 
  and all comments and optimizations are more then welcome.

TODOs:
  - Testing of icon classes in ie7
  - Further Documentation
  - Demo-Page
