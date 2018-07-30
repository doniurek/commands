# [⬅ Back	to Unix commands](unix.md)
# `time`
Report the duration of execution of a particular command/program

`time <command>`

## Options
`-o <file>` write the resource use statistics to &lt;file&gt; instead of to the standard error stream. By default, this overwrites the file, destroying the file's previous contents

`-a` append the resource use information to the output file instead of overwriting it

`--quiet` do not report the status of the program even if it is different from zero

## Example
`time ls`
>git.md  README.md  unix\
>\
real	0m0.002s\
user	0m0.000s\
sys	0m0.000s
