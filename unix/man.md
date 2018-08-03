# [⬅ Back	to Unix commands](unix.md)
# `man`
Display system documentation

## Options
`-a` Display, in succession, all of available manual pages contained within the manual.

`-f` Display a short description from the manual  page(s), if available.

`-k <keyword(s)>` Search the short manual page descriptions for &lt;keyword(s)&gt; and display any matches.

`-K <keyword(s)>` Search for &lt;keyword(s)&gt; in all manual pages. This is a brute-force search, and is likely to take some  time.

`-s <list>` List is a colon- or comma-separated list of 'order specific' manual sections to search/display.

## Example
`man -f intro` Display a short description from the manual  pages of *intro*
```
intro (7)            - introduction to overview, conventions, and miscellany section
intro (5)            - introduction to file formats
intro (6)            - introduction to games
intro (2)            - introduction to system calls
intro (8)            - introduction to administration and privileged commands
intro (4)            - introduction to special files
intro (1)            - introduction to user commands
intro (3)            - introduction to library functions
```

`man -s 6 intro` Show "introduction to games" section

## Comments
Press `/` to search phrase on displayed manual page
