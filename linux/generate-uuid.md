# Generate an UUID (2016-02-12)

It's as easy as running `uuidgen`:
```bash
uuid=$(uuidgen)
echo $uuid
```

It's part of [`uuid-runtime`](https://packages.debian.org/sid/uuid-runtime) on Debian. On OS X, it seems to be built-in.

If `uuidgen` is not available for some reason, the same can be achieved with Python:
```bash
python  -c 'import uuid; print uuid.uuid1()'
```