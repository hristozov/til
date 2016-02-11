# Get directory of current script (2016-06-11)
Can be done by getting the directory part of `__file__` or `sys.argv[0]`, in case the former is not available:

`os.path.dirname(os.path.realpath(__file__))` 

`os.path.dirname(os.path.realpath(sys.argv[0]))`

[Thank you, Stack Overflow!](https://stackoverflow.com/questions/4934806/how-can-i-find-scripts-directory-with-python)