# [⬅ Back	to Unix commands](unix.md)
# `split`
Split a file into pieces

`split <file> [prefix]`

Output  pieces  of  &lt;file&gt;  to *[prefix]aa*, *[prefix]ab*, etc.\
Default size is 1000 lines, and default prefix is 'x'

## Options
`-a <num>` generate suffixes of length &lt;num&gt; (default 2)

`-b <size>` put &lt;size&gt; bytes per output file

`-C <size>` put at most &lt;size&gt; bytes of records per output file

`-d` use numeric suffixes starting at 0, not alphabetic

`--numeric-suffixes[=FROM]` same as `-d`, but allow setting the start value

`-l <number>` put &lt;number&gt; lines/records per output file

`-n <chunks>` generate &lt;chunks&gt; output files; chunks may be:
- N - split into N files based on size of input
- K/N - output Kth of N to standard output
- l/N - split into N files without splitting lines/records
- l/K/N - output Kth of N to standard output without splitting lines/records

`-t <separator>` use &lt;separator&gt; instead of newline as the record separator

## Examples
`split -dn l/4 test.txt part`
split file test.txt into 4 files: part00, part01, part02, part03 without splitting lines

## Comment
The  &lt;size&gt; argument is an integer and optional unit (example: 10K is 10*1024). Units are K,M,G,T,P,E,Z,Y (powers of 1024) or KB,MB,... (powers of 1000).
