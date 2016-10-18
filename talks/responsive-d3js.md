# Reponsive d3.js

Flash.Is.Dead

## Why was flash so popular?

- Simple to use and animate
- Vector graphic & streaming and video

## Data Driven Documents

### D3 is NOT

* Chart Library
* render things for you
* for IE8 & below (use `sizzle` for compatibility)

### D3 is...

* a combination of building blocks (modules)
* great tool for mapping data to the DOM
* transform the data
* Smooth transition between UI states

## D3 in the web

There are loads of great examples of D3 on the web.

http://therefugeeproject.org - The Refugee Project is a great example


Load it with

* Use loader from the website
* Minified version
* NPM

Using modules vs deafult bundle

* Default bundle (script tag)
* Module

```javascript
var day = d3.timeDay(new Date);
```

* Function

```javascript
import { extent } from 'd3-array';
```

## What do you need to know?

* SVG
* CSSS
* JS
* HTML
* npm

## Population of New England by state

### Data

Can be represented in many ways

* Array
* JSON Object

```javascript
myData = [{
  "name": "Massachusets"
}]
```

### Selection

Selects elements and attaches data

```html
<div class="chart">
  <p>I am a paragraph</p>
</div>
```

```javascript
d3.select("p");
d3.selectAll("p");
d3.select(".chart").selectAll("p")
```

### CSS3 as a selectio tool

```javascript
d3.selectAll("circle").attr("r", 25);
d3.select("input[typecheckbox]").checked(true)
```

Set or modify attributes, styles, properties, HTML or text content.

### Control Flow:

* `.call();` - calls a function on the selection

```javascript
function showAlert(){}

d3.select(".chart").selectAll("p").call(showAlert)
```

* Elements can be `added` or `removed` from a selection

* Manipulating text
 
```javascript
var d3 = d3.selectAll(".chart");
d3.append("p").text("d3 is awesome!");
```

## Data Joins

Each datum from the set of data will be bound to a selection.

```javascript
var myData = [1,25,75];
// Entered 1,25,75

var myData = [1,25,75,45,150];
// updated 1,25,75 and Entered 45,150
```

1. Select an element that you want to bind to

```javascript
var myData = [1,25,75];
var dataJoin = d3.selectAll("div")

dataJoin.data(myData);
```

`enter()` or `exit()`

```javascript
var bar = d3.selectAll(".bar").data(data);
bar.enter().append("div").attr("class", "bar");

// Exit
bar.exit().remove();
```

### General Visualization Pattern

* `d3.selectAll("div")` - select the element
* `.data(data)` - bind the data
* `.enter()` - create a DOM element
* `.append("div")` - Output the data onto the screen

### SVG Viewport

SVG renders it's elements starting from the top left corner (vertically flipped from the mathematical coordinate space).

### SVG Group Transform

Allows us to transform particular elements within a group inside of the SVG.

### Scales

Check Quantile, Quantize, Threshold Scales.

```
domain:[625741, 1252567, 1316470]
range:[1,5,10]
```

* Continuous (Linear, Power, Log, Identity, Time)

  Map a continous, quantitiative input domain toa continuous output range.
  
* Ordinal (Band, Point, Category)

  discrete types of information like names.

### Initial Visualization decision based on data

* What is independent variable?
* What is dependent variable?

## Making SVG Repsonsive

* Make SVG responsive
`preserveAspectRatio="xMinYMin meet" viewBox="0 0 800 960"`
* SVG re-draw depends on the screen re-size (better)
* Use aspect ratio based on window size instead of px
* Breakpoints for visualization changes

## Animation

GSAP for animation. D3 can do this, but GSAP is better at this.

* Mike Bostock
* Building Responsive Data Visualizations with D3.js
* DashingD3js Screencasts
* D3.js tutorials
