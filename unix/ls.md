# [⬅ Back	to Unix commands](unix.md)
# `ls`
List  information about the file(s) (the current directory by default)

`ls [file]`

## Options
`-a` do not ignore entries starting with .

`-A` do not list implied . and ..

`-C` list entries by columns

`--color=<always/auto/never>` colorize the output. With `auto` ls emits color codes only when standard output is connected to a terminal.

`-F` append indicator (one of \*/=>@|) to entries, whih means e.g.
* @ symbolic link (or that the file has extended attributes).
* \* executable
* = socket
* | named pipe
* / directory

`-h` with `-l` and/or `-s` print human readable sizes

`-i` print the index number of each files

`-l` use a long listing format

`-R` list subdirectories recursively

`-s` print the allocated size of each file, in blocks

`-S` sort by file size, largest first

`-t` sort by modification time, newest first

## Comments
In Ubuntu there are default aliases:

`l='ls -CF'`

`la='ls -A'`

`ll='ls -alF'`

`ls='ls --color=auto'`
