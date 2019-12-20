# doxygen-template

A Doxygen template for an API with a user manual. 

## Installing Doxygen 

On macOS, you can install Doxygen with Homebrew:

```
brew install doxygen 
```

Otherwise, use the official install [instructions](http://www.doxygen.nl/download.html).

## Structure 

* Manual 
* Overview
* Topic


### Integrating Into a Project

I prefer to keep documentation with the codebase whenever reasonably possible. 

```
API
 |- build
 |- docs
     |- images
     |- snippets
     |- 
 |- inc
 |- src
```


## Conventions 

* Pure Doxygen files use the file extension `*.dox`
*
*  
