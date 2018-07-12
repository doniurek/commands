# [⬅ Back	to Unix commands](unix.md)
# `chown`
Change the user and/or group ownership of each given file

`chown <user>`
`chown <user>:<group>`
`chown :<group>`

## Options
`-R` change files and directories recursively
`-f` forge ahead with all objects even if errors occur
`-v` show objects processed

## Examples
`chown donia /u` change the owner of __/u__ to __donia__

`chown -R donia /u` change the owner of __/u__ and subfiles to __donia__


## Comments
Be carefull about symbolic links
