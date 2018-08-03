# [⬅ Back	to Unix commands](unix.md)
# `tail`
Output the last part of file(s)

`tail <file(s)>` (without options) print the last 10 lines of each file to standard output. With more than one file, precede each with a header giving the file name

## Options
`-c <num>` output the last &lt;num&gt; bytes

`-c +<num>` output starting with byte &lt;num&gt; of each file

`-n <num>` output the last &lt;num&gt; lines, instead of the last 10

`-n +<num>` output starting with line &lt;num&gt;

`-q` never output headers giving file names

`-v` always output headers giving file names

## Examples
`cat test.txt`
```
a
b
c
d
e
f
g
h
i
j
k
```

`tail -n 5 test.txt`
```
g
h
i
j
k
```

`tail -n +5 -v test.txt `
```
==> test.txt <==
e
f
g
h
i
j
k
```
