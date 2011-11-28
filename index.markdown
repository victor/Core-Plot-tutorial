---
title: Core Plot Tutorial
layout: default
---

# Core Plot Tutorial

This tutorial will show you how to get started using Core Plot in your projects. I will explain how to use it on an iOS project, but if you want to use it on a Mac application, it will be useful as well, as Core Plot has abstracted the differences between the platforms, so what you learn for one platform will be useful also for the other one.

## Obtain the libraries

When we go to the Core Plot home page at http://code.google.com/p/core-plot/, we see a featured download of the relase 0.9, named `CorePlot_0.9.zip`. Core Plot is about to release version 1.0, so by the time you read this that could very well be the current version. In any case, grab the file and unzip it, and take note of where you did that.

## Getting started

To begin, let’s create a Single View based iPad app project. I chose an iPad app because it has a bigger screen and allows me to better show what I’m telling. Feel free to follow along on an iPhone project – as long as you change the dimensions appropriately.

![Figure 1: Creating a Single View project](images/00_new_project_options.png)

## Adding the libraries

The next step is to add the Core Plot libraries to your project. When Core Plot was in heavy development, it changed very fast, so it made sense to incorporate it as a subproject of ours, and made it a dependency so that it was rebuilt every time it changed. Nowadays, with the final 1.0 release so close, it makes more sense to just add it as a static library. To do that, open the Finder where you unpacked the Core Plot zip file, and navigate to the `Binaries/iOS` directory. Then, drag the 

I like to put all my external libraries in an Xcode group, which I call “3rd Party”. Drag the `libCorePlot-CocoaTouch.a` file and the `CorePlotHeaders` folder into your project, and enable the copying of the files and the creation of groups for nested folders. These options are again a matter of taste, if you want your project to be self-contained, then make sure to make a copy and not to just reference the dependencies. On the other hand, if you use the library heavily and want to make sure that it is updated in your projects whenever you update it, by all means just use a reference. 