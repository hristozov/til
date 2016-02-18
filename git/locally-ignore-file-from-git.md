# Ignore a file from git (2016-02-17)
Can be done with:

`git update-index --assume-unchanged <file>`

This way the file will remain there, but git won't track any changes.

To undo the action:

`git update-index --no-assume-unchanged <file>`

You can see all ignored files in the current repository with:

`git ls-files -v | grep '^[[:lower:]]'`
