# Catch a signal (2016-02-12)

You can catch signals in bash using `trap`:

```bash
#!/bin/bash 

_handler() { 
  echo "Wow!"
}

trap _handler SIGTERM
```

It can be useful for manipulating children processes or Docker containers started by a script.