# [⬅ Back	to Unix commands](unix.md)
# `tee`
Read from standard input and write to standard output and files

`tee <file(s)>`

Copy standard input to each &lt;file&gt; and also to standard output

## Options
`-a` append to the given &lt;file&gt;, do not overwrite

`-i` ignore interrupt signals

`-p` diagnose errors writing to non pipes

## Example
`tee test.txt`
open interactive session

`Here, for now, is stubble`

>Here, for now, is stubble\
Here, for now, is stubble

`cat test.txt`
>Here, for now, is stubble

`tee -a test.txt test2.txt`
open interactive session

`But it will be San Francisco`

>But it will be San Francisco\
But it will be San Francisco

`cat test.txt`
>Here, for now, is stubble\
But it will be San Francisco

`cat test2.txt`
>But it will be San Francisco

`echo -e "Ann 158\nBob 175\nGreg 179" | grep 17[0-9] | tee testee.txt | grep Greg`
>Greg 179

`cat testee.txt `
>Bob 175\
Greg 179
