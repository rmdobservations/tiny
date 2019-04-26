# Using tiny

I found a tutorial about making a simple npm package. 
This was based on tutorial by https://medium.freecodecamp.org/how-to-make-a-beautiful-tiny-npm-package-and-publish-it-2881d4307f78

Some things I noticed but were not explicitly pointed out by original author. In particular, I was confused by the combination of creating the package, **tiny** and the using of **tiny** in the section **Usage**. It is clear to me now that the **Usage** code had to be in a different project. But I am new at this so I was confused. 

The README for creating **tiny** are on the npm site at: https://www.npmjs.com/package/@izziedee1/tiny
 

# Instructions for using **tiny** package
## New project with name rmd1

1. Create new directory with same name as project and cd into it:
```
     mkdir rmd1
     cd rmd1
```
2. Create file **index.js** and enter this code: 
 ```javascript 
      const tiny = require("@izziedee1/tiny");
      console.log(tiny("So much space!")); 
  ```
3. Use init to create a new _package.json_ for project **rmd1**:
``` 
npm init --scope=izziedee1
```
4. The resulting package.json will look like:
```json
{
  "name": "@izziedee1/rmd1",
  "version": "1.0.0",
  "description": "First test package",
  "main": "index.js",
  "scripts": {
    "test": "node rmdtest.js"
  },
  "repository": {
    "type": "git",
    "url": "rmdobservations"
  },
  "author": "rose",
  "license": "ISC",
  "dependencies": {
    "@izziedee1/tiny": "^1.0.0"
  }
}
```

5. To check if this works, run at command line, 
```
node index
 ```
6. Should see output at console:  
```
Somuchspace!
```
# Discussion

Creating a github repository distracted from the goal of the essay. Messing around with npm account caused some stupid errors.
I did achieve my goal of learning how to create a package and use it.

# OS
I ran this in Ubuntu Linux 18.04



