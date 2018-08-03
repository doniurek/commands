# [⬅ Back	to Unix commands](unix.md)
# `chmod`
Change the file modes/attributes/permissions

## Options
`-R` change files and directories recursively

`-f` forge ahead with all objects even if errors occur

`-v` show objects processed

## Comments
To view the file mode the `ls -l <file or directory>` command may be used.
```
drwxr-xr-x  2 donia donia   4096 lut 19  2017 Muzyka
drwxr-xr-x  2 donia donia   4096 lut 19  2017 Obrazy
drwxr-xr-x  3 donia donia   4096 lip  7 15:23 Pobrane
```

The __r__, __w__, and __x__ specify the __read__, __write__, and __execute__ access

The left three characters define permissions of the __OWNER__,

next three characters define permissions of the __GROUP__

and next three - permissions of __EVERYONE ELSE__.

Last digit is something I don't know yet xD

## Examples

### Numeric mode
| # |	Permission	| rwx |
| ----- | ----- | ----- |
| 7 |	read, write and execute	| rwx |
| 6 |	read and write	| rw- |
| 5 |	read and execute	| r-x |
| 4 |	read only	| r-- |
| 3 |	write and execute	| -wx |
| 2 |	write only	| -w- |
| 1 |	execute only	| --x |
| 0 |	none	| --- |

`ls -l sharedFile` → show acces modes before chmod
```
-rw-r--r--  1 jsmith programmers 57 Jul  3 10:13  sharedFile
```

`chmod 664 sharedFile`

`ls -l sharedFile` → show acces modes after chmod
```
-rw-rw-r--  1 jsmith programmers 57 Jul  3 10:13  sharedFile
```

### Symbolic mode
| Reference |	Class |	Description |
| ----- | ----- | ----- |
| u |	owner |	file's owner |
| g |	group |	users who are members of the file's group |
| o |	others |	users who are neither the file's owner nor members of the file's group |
| a |	all |	all three of the above, same as ugo |

| Operator | Description |
| ----- | ----- |
| + |	adds the specified modes to the specified classes |
| - |	removes the specified modes from the specified classes |
| = |	the modes specified are to be made the exact modes for the specified classes |


`ls -ld shared_dir`
```
drwxr-xr-x   2 teamleader  usguys 96 Apr 8 12:53 shared_dir
```

`chmod  g+w shared_dir` → add write permission for group

`ls -ld shared_dir`
```
drwxrwxr-x   2 teamleader  usguys 96 Apr 8 12:53 shared_dir
```

---

`ls -l ourBestReferenceFile`
```
-rw-rw-r--   2 teamleader  usguys 96 Apr 8 12:53 ourBestReferenceFile
```

`chmod a-w ourBestReferenceFile` → remove write permissions for all classes

`ls -l ourBestReferenceFile`
```
-r--r--r--   2 teamleader  usguys 96 Apr 8 12:53 ourBestReferenceFile
```
