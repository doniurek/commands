# [⬅ Back	to Unix commands](unix.md)
# `du`
Estimate file space usage

Summarize disk usage of file(s), recursively for directories.

## Options
`-c` produce a grand total (sum of all input files space usage)

`-h` print sizes in human readable format (e.g., 1K 234M 2G)

`-s` report only the sum of the usage in the current directory, not for each directory therein contained

## Examples
`du -h Desktop/`
```
16K	Desktop/dir1
20K	Desktop/dir2
8,0K	Desktop/others/may/silver
44K Desktop/
```

`du -hs Desktop/`
```
44K Desktop/
```

`du -ch Desktop/`
```
16K	Desktop/dir1
20K	Desktop/dir2
8,0K	Desktop/others/may/silver
44K Desktop/
44K total
```
