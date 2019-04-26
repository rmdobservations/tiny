# tiny
Tutorial I was following left me in the dark about how to put this badge anywhere. I found a discussion from which I created this badge. 

[![Build Status](https://img.shields.io/npm/v/tiny.svg)](https://github.com/rmdobservations/tiny)

This one was made from copying markdown. Makes more sense. But clicking on it gives me just the image. The one above takes me to my github repository.

![npm](https://img.shields.io/npm/v/tiny.svg)

# Instructions
Put this code into a files called index.js (See Discussion)


>const tiny = require("@rmdobservations/tiny");

>tiny("So much space!");
>//=> "Somuchspace!"

>tiny(1337);
>//=> Uncaught TypeError: Tiny wants a string!
>//    at tiny (<anonymous>:2:41)
>//    at <anonymous>:1:1

# Discussion

This was based on tutorial by https://medium.freecodecamp.org/how-to-make-a-beautiful-tiny-npm-package-and-publish-it-2881d4307f7

Some things I noticed but were not explicitly pointed out by original author.

 

Not clear was the separation between the folder called **tiny** and the creation of another folder when
installing  **tiny** as a module. 

├── node_modules
│   └── @rmdobservations
│       └── tiny
│           ├── index.js
│           ├── package.json
│           ├── README.md
│           └── tiny-version-brightgreen.svg

There are two package.json files. One is in the tody folder itself. The other is created in another directory which will access the tidy package. This part was unclear.

## other directory
Create a package.json for a new project:
**npm init ** 

Install **tiny** in node_modules

**npm install @rmdobservations/tiny**
creates this tree structure

testingNPM$ tree
.
└── node_modules
    └── @rmdobservations
        └── tiny
            └── package.json

Create index.js using code in **Instructions** above. Leave out error messages. 
Run at command line: **nodejs index.js**
does not work. I am missing in my project **package.json**. How did it get there?

>"dependencies": {
>    "@rmdobservations/tiny": "file://tiny"
>  }

## Start over in a new directory

In directiry **testnpm** Create index.js from code from introduction

**testnpm$** npm init
_Creates a package.json file_
**testnpm$** npm install @rmdobservations/tiny --save
_testingnpm@1.0.0 /testingNPM
└── @rmdobservations/tiny@1.0.0  extraneous_

Adding the --save cause dependency to be written into project testnpm's **package.json**
 >"dependencies": {
  >  "@rmdobservations/tiny": "^1.0.0"

This is different from the original package.json
>"dependencies": {
>    "@rmdobservations/tiny": "file://tiny"


# Particular
I ran this in Ubuntu Linux 18.04

# Critique
Creating a github repository distracted from the goal of the essay.
