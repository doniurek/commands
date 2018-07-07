# [⬅ Back	to Unix commands](Unix.md)
# `chgrp`
Change the file group ownership

## Options
`-R` operate on files and directories recursively
`-f` forge ahead with all objects even if errors occur
`-v` show objects processed

## Examples
`chgrp staff /u` change the group of __/u__ to __staff__ group

`chgrp -R staff /u` change the group of __/u__ and subfiles to __staff__ group

## Comments
Be carefull about symbolic links
