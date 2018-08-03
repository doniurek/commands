# [⬅ Back	to Unix commands](unix.md)
# `comm`
Compare two __sorted__ files line by line

## Options
`-1` suppress column 1 (lines unique to FILE1)

`-2` suppress column 2 (lines unique to FILE2)

`-3` suppress column 3 (lines that appear in both files)


## Examples
`cat file1.txt`
```
apple
banana
eggplant
```

`cat file2.txt`
```
apple
banana
banana
zucchini
```

`comm file1.txt file2.txt`
```
                     apple
                    banana
            banana
    eggplant
            zucchini
```


`comm -12 file1.txt file2.txt` Print only lines present in both file1 and file2
```
banana
zucchini
```

`comm -3 file1.txt file2.txt` Print lines in file1 not in file2, and vice versa.
```
apple
banana
eggplant
```
