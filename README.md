# Michelangelo Styleguide
[![npm version](https://badge.fury.io/js/michelangelo.svg)](https://badge.fury.io/js/michelangelo)



## Table of contents
- About
- Get started
- Usage
    + KSS-node and documentation syntax
    + Michelangelo specifications
- Demo



## About
A custom template for the kss-node living style guide.



## Get started
If you are new to KSS-node, install it globally with `npm install -g kss`. Then go to your project directory and install the plugin locally.
```
npm install michelangelo --save-dev
```

Create a config file `kss-config.json` and specify the following config. Read [the KSS-node docs](https://github.com/kss-node/kss-node#using-the-command-line-tool) for more information about the config.
```
{
  "title"       : "Michelangelo Styleguide",
  "mask"        : "*.scss",
  "placeholder" : "[modifier]",

"//": "relative to this file.",
  "homepage"     : "kss-styleguide.md",
  "builder"      : "kss_styleguide/custom-template/",
  "source"       : "src/",
  "destination"  : "kss_styleguide/styleguide/",

"//": "relative to the generated style guide.",
  "css": [],
  "js" : []
}
```

After setting up the config file, run `kss --config kss-config.json` to generate your living styleguide. Locate your styleguide at the specified path in your config file and open it in the browser.



## Usage

### KSS-node and documentation syntax
KSS-node is an implementation of Knyle Style Sheets. A documentation syntax for css that can be used to create a living style guide. KSS-node has a few additional features such as adding a copy of the markup inline or external.

To get familiar with the documentation syntax it is highly advised to read trough [the annotated copy of the official KSS spec on the kss-node repository](https://github.com/kss-node/kss/blob/spec/SPEC.md).


### Michelangelo specifications

#### Color grid
A grid overview of all your project colors. Every color item consists of 4 parts, with the color variable and hexadecimal required:
- color example
- color name
- color variable
- color hexadecimal

In the example below you can see we have a heading, a description and that we list our colors below with a color description after the dash. To make the colors work you must first define your hexadecimal, then optionally add an color name.
```scss
// Primary Colors
//
// The primary colors for branding.
//
// $leonardo      -  #2980b9, Leader blue
// $donatello     -  #8e44ad, Purple tech
// $raphael       -  #c0392b, Sai
// $michelangelo  -  #E87E04, Cowabunga
// $splinter      -  #FDE3A7
//
// Styleguide Settings.Colors
```

#### Responsive
The specific styling for the styleguide is written mobile first. Which makes it possible to test your project's styling directly on any device size.

#### Smooth scrolling
When clicking on a sub navigation item the page animate scrolls to that specific item, so smooooth.

#### ITCSS architecture
The example src directory is a boilerplate for [ITCSS methodology](https://youtu.be/1OKZOV-iLj4). A methodology created by Harry Roberts.



## Demo
Have a look at [the demo styleguide](http://stamkracht.github.io/michelangelo/) generated with dummy content to get an impression of the Michelangelo theme with the ITCSS architecture.
