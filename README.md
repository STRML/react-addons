# react-addons

This is an npm package containing *only* the react addons, and not the full react build
itself (although it requires it). This will play much more nicely with browserify
and other build tools than the old `require('react/addons')` style.

This package is a direct copy/paste of the files in `lib/`, with the paths to `/React` changed
to require the base `react` module. If this module gets significantly out of date, it should
be simple to rebuild using the React source.

## Example Usage

```js

// Previously, you might access React Addons with this path.
var React = require('react/addons');

// Now, you can access it this way:
var addons = require('react-addons');

// And the addons are available directly on the module, like so:
var classSet = require('react-addons').classSet;

// Now, you don't have to worry about changing all your `require` statements
// throughout your app to use `react/addons`!
```
