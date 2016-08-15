# Cancel requestAnimationFrame() (2016-08-15)

`requestAnimationFrame()` returns an ID which can be used to cancel the "request" later, using `cancelAnimationFrame()`:

```javascript
var id = window.requestAnimationFrame(function() { ... });
...
cancelAnimationFrame(id);
```

Of course, this works on _modern_ browsers.
