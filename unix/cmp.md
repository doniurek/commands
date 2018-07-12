# [⬅ Back	to Unix commands](unix.md)
# `cmp`
Compare two files

`cmp <file1> <file2>`

## Options
`-b` print differing bytes
`-i <skip>` skip first &lt;skip&gt; bytes of both inputs
`-i <skip1>:<skip2>` skip first &lt;skip1&gt; bytes of &lt;file1&gt; and first &lt;skip2&gt; bytes of &lt;file2&gt;

## Examples
`cmp -i 30 test1.txt test2.txt`
> test1.txt test2.txt differ: byte 1, line 1
