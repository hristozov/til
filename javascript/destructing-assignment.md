# Destructing assignment (2016-02-18)
A relatively insignificant, but neat feature is the destructing assignment:
```javascript
var things = [ "foo", "bar", "baz" ],
 [ first, , last ] = things;

// now swap them
[ last, first ] = [ first, last ]
```

Unfortunately, this syntax is not supported by Node yet.
