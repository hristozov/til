# Find or replace a substring with `String#[]`/`String#[]=` (2016-08-17)

The [`String#[]`](http://ruby-doc.org/core-2.2.0/String.html#method-i-5B-5D) method can match substrings, using a string or `RegExp` for matching.
In the same manner [`String#[]=`](http://ruby-doc.org/core-2.2.0/String.html#method-i-5B-5D-3D) can replace the match.
```
[1] pry(main)> str = "Hello, Georgi"
=> "Hello, Georgi"
[3] pry(main)> str['Georgi']
=> "Georgi"
[4] pry(main)> str['Georgi'] = 'Ivan'
=> "Ivan"
[5] pry(main)> str
=> "Hello, Ivan"
```
The replacement can make the string longer:
```
[6] pry(main)> str[/[A-Z]/]
=> "H"
[7] pry(main)> str[/[A-Z]/] = 'Ze'
=> "Ze"
[8] pry(main)> str
=> "Zeello, Ivan"
```

A `nil` is returned if there is no match. `String#[]=` raises an `IndexError` in this case:
```
[9] pry(main)> str['H']
=> nil
[10] pry(main)> str['H'] = 'Me'
IndexError: string not matched
from (pry):8:in `[]='
```

Somehow I've missed that one, although it's currently featured in one of the examples on the [official Ruby website](https://www.ruby-lang.org/en/)!
