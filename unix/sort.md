# [⬅ Back	to Unix commands](unix.md)
# `sort`
Sort, merge, or sequence check text files

`sort <file(s)>`

Write sorted concatenation of all &lt;file(s)&gt; to standard output

## Options
`-d` consider only blanks and alphanumeric characters

`-f` fold lower case to upper case characters

`-g` compare according to general numerical value

`-i` consider only printable characters

`-k <key>` sort via a key, e.g. sort on a certain column
- `-k <m>,<n>` sort on a key that is potentially composed of multiple fields (start at column m, end at column n)

`-h` compare human readable numbers (e.g., 2K 1G)

`-n` sort according to numerical value

`-r` reverse the result of comparisons

`-t <separator>` use &lt;separator&gt; instead of non-blank to blank transition

`-c` check for sorted input; do not sort

`-m` merge already sorted files; do not sort

`-o <file> `write result to &lt;file&gt; instead of standard output

## Example
`cat zipcode`
```
Adam  12345
Bob   34567
Joe   56789
Sam   45678
Wendy 23456
```

`sort -nk 2 zipcode`
```
Adam  12345
Wendy 23456
Bob   34567
Sam   45678
Joe   56789
```

`sort -k2,2 -t $'\t' phonebook`
```
Fogarty, Suzie	555-2314
Doe, Jane	555-3214
Avery, Cory	555-4132
Smith, Brett	555-4321
```

`sort -rnk 2 zipcode`
```
Joe   56789
Sam   45678
Bob   34567
Wendy 23456
Adam  12345
```
