# viewability

Browser package to check if the element is on screen without dependencies. Or you can call it visibility.

[![npm version](https://badge.fury.io/js/viewability.svg)](https://www.npmjs.com/package/viewability)
[![Bower version](https://badge.fury.io/bo/viewability.svg)](http://badge.fury.io/bo/viewability) 
[![devDependency Status](https://david-dm.org/kahwee/viewability/dev-status.svg)](https://david-dm.org/kahwee/viewability#info=devDependencies)

No dependencies.

```js
var vertical = require('viewability/vertical');
vertical(document.getElementById('blue-box'));
// return {value: 1, state: "EL_IS_WITHIN_VERTICAL_VIEW"}
```

Use `'viewability/horizontal'` for corresponding view.

[See demo](https://kahwee.github.io/viewability/)

# Installation

* [Bower](http://bower.io/): `bower install --save viewability`
* [npm](https://www.npmjs.org/): `npm install --save viewability`
* Direct download the latest version: https://github.com/kahwee/viewability/releases
* [jsDelivr CDN](http://www.jsdelivr.com/#!viewability): `<script src="//cdn.jsdelivr.net/viewability/VERSION/viewability.min.js"></script>`

# Usage

## `viewability` package through CDN:

Loading it directly to the browser with `viewability` exposed to the window:

```html
<script src="//cdn.jsdelivr.net/viewability/latest/viewability.min.js"></script>
<script>
  var v = viewability.vertical(document.getElementById('red-box'));
  console.log(v);
  // return {value: 0.83, state: "EL_IS_WITHIN_VERTICAL_VIEW"}
</script>
```

## Using Common JS:

Finding out if the element is 100% on screen and using Common JS:

```js
var v = require('viewability');
var el = document.getElementById('blue-box');
if (v.isElementOnScreen(el, true)) {
  console.log('100% on screen.');
} else if (v.isElementOnScreen(el)) {
  console.log('Some parts are on screen');
} else {
  console.log('not on screen at all');
}
```

# Running tests

While `viewability` has no dependencies, testing uses Karma and jQuery.

```sh
npm install
npm test
```

# License

ISC
