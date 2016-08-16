# Sort "human-readable" sizes (2016-08-16)
([Source](https://serverfault.com/questions/62411/how-can-i-sort-du-h-output-by-size))

The `sort` command has a `-h` switch which allows it to sort "human-readable" sizes in the output of other commands:
```
$ du -cksh
220K   	argparse
 36K   	balanced-match
 32K   	base64-js
 24K   	brace-expansion
 28K   	concat-map
 68K   	glob
 24K   	inflight
 24K   	inherits
2.1M   	lodash
 44K   	minimatch
 64K   	mkpath
 20K   	node-version-compare
 16K   	once
 16K   	path-is-absolute
516K   	plist
 24K   	rimraf
 76K   	sax
 76K   	underscore
 72K   	underscore.string
 24K   	util-deprecate
 20K   	wrappy
4.5M   	xml2js
104K   	xmlbuilder
100K   	xmldom
936K   	yamljs
9.1M   	total

$ du -cksh * | sort -h
 16K   	once
 16K   	path-is-absolute
 20K   	node-version-compare
 20K   	wrappy
 24K   	brace-expansion
 24K   	inflight
 24K   	inherits
 24K   	rimraf
 24K   	util-deprecate
 28K   	concat-map
 32K   	base64-js
 36K   	balanced-match
 44K   	minimatch
 64K   	mkpath
 68K   	glob
 72K   	underscore.string
 76K   	sax
 76K   	underscore
100K   	xmldom
104K   	xmlbuilder
220K   	argparse
516K   	plist
936K   	yamljs
2.1M   	lodash
4.5M   	xml2js
9.1M   	total
```
On OS X the built-in `sort` does not support `-h`. Fortunately, the GNU sort can be used as `gsort` after `coreutils` are installed:
```
$ brew install coreutils
$ du -cksh * | gsort -h
```
