# [⬅ Back	to Unix commands](unix.md)
# `cut`
Cut out (print) selected fields __of each line__ of a file

## Options
`-b <list>` select only these bytes

`-c <list>` select only these characters (e.g. from 1st to 10th)

`-d <delimiter>` use custom <delimiter> instead of TAB for field delimiter
  
`-f <list>` select  only  these  fields (e.g. columns)

Use  one,  and  only  one  of  `-b`, `-c` or `-f`.  Each LIST is made up of one range, or many ranges separated by commas.

Each range is one of:
* __N__      N'th byte, character or field, counted from 1
* __N-__     from N'th byte, character or field, to end of line
* __N-M__    from N'th to M'th (included) byte, character or field
* __-M__     from first to M'th (included) byte, character or field

## Examples
`cat test.txt`
```
foo;bar;baz;qux;quux
one;two;three;four;five;six;seven
alpha;beta;gamma;delta;epsilon;zeta;eta;theta;iota;kappa;lambda;mu
the quick brown fox jumps over the lazy dog
```

`cut -c 4-10 file`
```
quux
five;six;seven
epsilon;zeta;eta;theta;iota;kappa;lambda;mu
the quick brown fox jumps over the lazy dog
```
