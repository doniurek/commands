# [⬅ Back	to Unix commands](unix.md)
# `who`
Show who is logged on

## Options
`-l` print system login processes

`-H` print line of column headings

`-q` all login names and number of users logged on


## Example
`who`
```
NAME     LINE         TIME             COMMENT
donia    tty8         2018-08-01 14:05 (:0)
donia    pts/0        2018-08-01 14:08 (:0)
donia    pts/1        2018-08-01 14:09 (:0)
```

`who -l`
```
LOGIN    tty1         2018-08-01 14:04              1545 id=tty1
```
