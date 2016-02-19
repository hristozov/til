# Mock `require` (2016-02-19)
A `require` in Node code can be mocked using the [mock-require](https://www.npmjs.com/package/mock-require) package:

```javascript
var mockRequire = require('mock-require');

mockRequire('foo', { /* mock export */ }});

var foo = require('foo');
```

Seems that it depends on monkey-patching [`Module._load`](https://github.com/nodejs/node/blob/0c113e8fde95ea0b61fe2c9864807a92cc4d3337/lib/module.js#L285). More information can be found [here](http://fredkschott.com/post/2014/06/require-and-the-module-system/). I wouldn't mess with `Module._load` outside of test code.
