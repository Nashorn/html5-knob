`<x-knob>` Web Component
========================

`<x-knob>` is a rotary web input component that can be controlled by dragging and rotating it (with the mouse pointer or touch input).

[Open the demo page!][demo]

[![Short demonstration GIF](./video.gif)][demo]

This component has been created as a proof-of-concept, as a simple base that can be improved upon. It is a more polished version of a [previous experiment](http://codepen.io/denilsonsa/pen/LVwWJM).

Features:

* Pure JavaScript code, no libraries used.
* Supports mouse input and touch input.
    * But does not support multiple fingers.
* Uses cutting-edge technology: [HTML5](http://www.html5rocks.com/) [Web Components](http://www.w3.org/wiki/WebComponents/) with [Shadow DOM](http://www.html5rocks.com/en/tutorials/webcomponents/shadowdom/) and [Custom element](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/).
    * [Works](http://webcomponents.org/) on Google Chrome and Opera.
    * [Does not work](http://webcomponents.org/) on Firefox, Safari, IE, Edge.
    * Using [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs/releases) as a set of polyfills and adding [`shim-shadowdom` to the CSS](https://github.com/Polymer/docs/issues/269) improves the compatibility and makes it work correctly on Firefox.
* Not production-ready!
    * Unless the incompatibilities can be ignored.
* Excellent example for learning the new web technologies.


How to use
----------

Open the [demo page][demo] and its [source-code](https://github.com/denilsonsa/html5-knob/blob/gh-pages/index.html). Study the demo to understand what this component is capable of.

Is it not enough? Dive into [xknob.js](https://github.com/denilsonsa/html5-knob/blob/gh-pages/xknob.js) and feel free to study how it works, and feel free to modify it to suit your needs. This repository is less like a fully packaged library and more like a starting point to let other people develop more stuff. Be sure to read [HTML5 Rocks tutorial on custom elements](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/).


Limitations
-----------

The current implementation is not very accessible. It requires a mouse or a touch interface. It would be great to apply [ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) guidelines.

The current implementation does not support keyboard input. It would be nice to allow the widget be focused (by tab-navigation) and changed using arrow keys and Home/End/PageUp/PageDown.

The current implementation does not support DOM0-style events (e.g. `xknob.oninput = function(){}` will not work). Using the modern `xknob.addEventListener('input')` works fine.

For some reason, using two fingers to zoom the page will not work if one of the fingers starts the touch on the knob.


Acknowledgements
----------------

This code is loosely inspired by [KaisarCode Rotate](https://github.com/KaisarCode/Rotate).

The usage of HTML5 custom elements is based on [HTML5 Rocks tutorial](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/), found through [W3C Wiki](http://www.w3.org/wiki/WebComponents/).

[Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API) proved to be an extremely valuable resource.

[demo]: http://denilsonsa.github.io/html5-knob/