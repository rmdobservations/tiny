# tiny
Tutorial I was following left me in the dark about how to put this badge anywhere. I found a discussion from which I created this badge. 

[![Build Status](https://img.shields.io/npm/v/tiny.svg)](https://github.com/rmdobservations/tiny)

This one was made from copying markdown. Makes more sense. But clicking on it gives me just the image. The one above takes me to my github repository.

![npm](https://img.shields.io/npm/v/tiny.svg)

# Instructions
const tiny = require("@bamblehorse/tiny");

tiny("So much space!");
//=> "Somuchspace!"

tiny(1337);
//=> Uncaught TypeError: Tiny wants a string!
//    at tiny (<anonymous>:2:41)
//    at <anonymous>:1:1
