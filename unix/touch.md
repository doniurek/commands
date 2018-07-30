# [⬅ Back	to Unix commands](unix.md)
# `touch`
Update file access and modification times to the current time

`touch <file>`

A &lt;file&gt; argument that does not exist is created empty (unless `-c` or `-h` is supplied)

## Options
`-a` change only the acces time

`-c` do not create any files

`-h` affect each symbolic link instead of any referenced file

`-m` change only the modification time

`-r <file>` use this file's times instead of current time

`-t <stamp>` use [[CC]YY]MMDDhhmm[.ss] instead of current time

## Example
`ls`
>git.md  README.md  unix

`touch test.txt`

`ls`
>git.md  README.md  test.txt  unix

`-touch -t 201404061230 test.txt00`
change access and modification times to 06.04.2014 at 12:30
