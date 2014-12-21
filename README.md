# Angular SVG round progressbar

AngularJS module that uses SVG to create a circular progressbar

## [Demo](http://crisbeto.github.io/angular-svg-round-progressbar/)

## Install

Include Angular and [roundProgress.min.js](https://raw.githubusercontent.com/crisbeto/angular-svg-round-progressbar/master/build/roundProgress.min.js) or [roundProgress.js](https://raw.githubusercontent.com/crisbeto/angular-svg-round-progressbar/master/build/roundProgress.js) in your page. You can use bower, or a script-tag:

`bower install angular-svg-round-progressbar`

or

`<script src="http://crisbeto.github.io/angular-svg-round-progressbar/roundProgress.min.js"></script>`


Add `angular-svg-round-progress` to your app's module dependencies:

```javascript
angular.module('someModule', ['angular-svg-round-progress'])
```

## Options

* `current` current progress, some value on the scope or a number
* `max` maximum value, some value on the scope or a number
* `radius` radius of the circle
* `color` hex color for the `current` value, example: `#45ccce`
* `bgcolor` hex background color, example: `#eaeaea`
* `stroke` specifies the thickness of the line
* `semi` boolean, specifies whether the progressbar should be a semicircle or a full circle
* `iterations` number of iterations for the animation. Set it to 1 for *no animation* and increase for slower animation. *(Optional, 50 by default)*
* `animation` the easing function that will be used. Default value is `easeOutCubic`, possible values:
    * linearEase
    * easeInQuad
    * easeOutQuad
    * easeInOutQuad
    * easeInCubic
    * easeOutCubic
    * easeInOutCubic
    * easeInQuart
    * easeOutQuart
    * easeInOutQuart
    * easeInQuint
    * easeOutQuint
    * easeInOutQuint
    * easeInSine
    * easeOutSine
    * easeInOutSine
    * easeInExpo
    * easeOutExpo
    * easeInOutExpo
    * easeInCirc
    * easeOutCirc
    * easeInOutCirc
* Since the `0.2.0` release this directive uses dynamic binding. For example, if you want to change the fill color at a certain value, you can use `color="{{ (current / max < 0.5) ? '#ff8080' : '#45ccce'" }}`.

### Example:

```html
<div
    round-progress
    max="max"
    current="current"
    color="#45ccce"
    bgcolor="#eaeaea"
    radius="100"
    stroke="20"
    semi="true"
    iterations="50"
    animation="easeInOutQuart"></div>
```

## Browser support

* Internet Explorer 9+
* Firefox 28.0+
* Chrome 31+
* Safari 5.1+
* and pretty much any browser that supports SVG


## Development

*  `npm install` to install development dependencies
*  `grunt` to build minified demo in build/
*  `grunt deploy` to build minified demo and push it to gh-pages branch


## Credits

* Erik Möller for the requestAnimationFrame shim
* [Modernizr](http://modernizr.com/) for the SVG support test
* [Kirupa](http://www.kirupa.com/forum/showthread.php?378287-Robert-Penner-s-Easing-Equations-in-Pure-JS-(no-jQuery)) for the easing function
* [opsb](http://stackoverflow.com/questions/5736398/how-to-calculate-the-svg-path-for-an-arc-of-a-circle) for some of the math
* [konsumer](https://github.com/konsumer) for build-system & deployment stuff
