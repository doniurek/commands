# [⬅ Back	to Unix commands](unix.md)
# `rm`
Remove files or directories

`rm <file(s)>`

By default, rm does not remove directories

## Options
`-f` ignore nonexistent files and arguments, never prompt

`-i` prompt before every removal

`-I` prompt once before removing more than three files, or when removing recursively

`--no-preserve-root` do not treat '/' specially

`--preserve-root` do not remove '/' (default)

`-r` / `-R` remove directories and their contents recursively

`-d` remove empty directories

`-v` explain what is being done

## Example
`rm file1 file2 file3`
