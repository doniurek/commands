# [⬅ Back	to Unix commands](unix.md)
# `wc`
Print newline, word, and byte counts for each file and a total line if more than one file is specified


## Options       
`-c` print the byte counts

`-m` print the character counts

`-l` print the newline counts

`-L` print the maximum line length

`-w` print the word counts

Counts are printed, always in the following order: newline, word, character, byte, maximum line length.

## Example
`cat test.txt`
```
one two
three
four
```
`wc -c test.txt`
```
19
```
`wc -cl test.txt`
```
    3    19
```
