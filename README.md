# doxygen-template

A Doxygen template for comprehensively documenting an API. 

## Installing Doxygen 

On macOS, you can install Doxygen with Homebrew:

```
brew install doxygen 
```

For other platforms, use the official install [instructions](http://www.doxygen.nl/download.html).

## Structure 

* `Manual.dox`: Arrangement of pages and corresponding subpages. 
* `Overview.dox`: Main page for documentation.
* `Topic[x].dox`: Topic pages individual topics.
* `GettingStarted.dox`: A starting point for someone first learning. 
* `ClassHierarchy`: A description of how the classes or modules fit together. 
* `ExampleApplictions.dox`: A collection of example applications and snippets. 
* `QuickReferenceGuide.dox`: A brief, concise overview of API, helpful for remembering syntax. 

### Integrating Into a Project

I prefer to keep documentation with the codebase whenever reasonably possible. 

```
API
 |- build
 |- docs
     |- images
     |- snippets
     |- Manual.dox
     |- [file].dox
 |- inc
 |- src
 |- Doxyfile
 |- Makefile
 |- ...
```

## Conventions 

* Pure Doxygen files use the file extension `*.dox`
* If the language supports the use of include or header files (e.g. \*.h, \*.hpp), doxygen comments for
source code should reside there. 

## Doxyfile

Change the following in the `Doxyfile`:

* `PROJECT_NAME` - Project name.
* `PROJECT_BRIEF` - Brief project description.
* `PROJECT_LOGO` - Location for project logo.
* `OUTPUT_DIRECTORY` - _I use `doc` and build within source, but some CI configurations may require a different location._
* `INPUT` - Input directories for source files. 
* `EXAMPLE_PATH` - The path for snippets.
* `IMAGE_PATH` - The path for images referenced in Doxygen comment blocks.

Personal configurations:

* `JAVADOC_AUTOBRIEF` - This uses the the first line of the Doxygen comment as the brief tag.  
* `TOC_EXPAND` - Currently set to `NO`, however, can be a helpful option to aid navigation. 
* `GENERATE_LATEX` - Currently set to `NO`.

## License

[MIT](LICENSE)
