# Kill a process group (2016-02-22)
To kill a process group in Node, just give `process.kill` the PID of the group with a negative sign:
```javascript
process.kill(-1337);
```
