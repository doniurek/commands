# [⬅ Back	to Unix commands](unix.md)
# `test`
Evaluate expressions - compare values and check file types

`test <expression>` or `[ <expression> ]`

`test` returns a status of 0 (true) or 1 (false)

## Example
`cat test.sh`
```bash
#!/bin/bash

read x
if [ $x -lt 10 ] ; then
        echo "digit"
else
        echo "numeral"
fi
```

`./test.sh`\
`7`
```
digit
```

`./test.sh`\
`27`
```
numeral
```

`cat test2.sh`
```bash
#!/bin/bash

echo "Enter file1 and file2 separated by space"
read file1 file2
if test $file1 -nt $file2 ; then
        echo "File1 is newer than file2"
else
        echo "File1 is older than file2"
fi
```

`./test2.sh`\
`~/somedirectory/somefile.txt ~/somedirectory/someotherfile.txt`
```
File1 is older than file2
```

## Comments
For full list of possible expressions which `test` can evaluate check `test` manual
