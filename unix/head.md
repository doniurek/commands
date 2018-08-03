# [⬅ Back	to Unix commands](unix.md)
# `head`
Output the first part of files

Print the first 10 lines of each file to standard output. With more than one file, precede each with a header giving the file name.

## Options
`-c <num>` print the first &lt;num&gt; bytes of each file; with the leading `-` print all but the last &lt;num&gt; bytes of each file

`-n <num>` print the first &lt;num&gt; lines instead of the first 10; with the leading `-` print all but the last &lt;num&gt; lines of each file

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
l
m
n
o
p
r
s
t
u
w
x
y
z
```

`head -n -12 test.txt`
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
l
```
