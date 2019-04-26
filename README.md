# tiny

This was based on tutorial by https://medium.freecodecamp.org/how-to-make-a-beautiful-tiny-npm-package-and-publish-it-2881d4307f7

Some things I noticed but were not explicitly pointed out by original author. In particular, I was confused by the combination of creating the package, **tiny** and the using of **tiny** as a package in another project.

# Instructions for using **tiny** package

1. Create new directory and cd into it:
     * mkdir rmd1
     * cd rmd1

2. Create a new package.json for project rmd1:
 * npm init --scope=izziedee1
 * create file index.js and enter this code: 
 ```javascript 
      const tiny = require("@izziedee1/tiny");
      console.log(tiny("So much space!")); 
  ```
3. At command line, 
 * node index
 
4. Should see output at console:  Somuchspace!

 # Discussion


# Particular
I ran this in Ubuntu Linux 18.04

# Critique
Creating a github repository distracted from the goal of the essay. Messing around with npm account caused some stupid errors.
