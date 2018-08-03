# [⬅ Back	to Unix commands](unix.md)
# `paste`
Merge corresponding or subsequent lines of files

## Options
`-d <delimiter(s)>` use &lt;delimiter(s)&gt; instead of TABs

`-s` paste one file at a time instead of in parallel

## Example
`cat name.txt`
```
Ann
Martha
Jacob
George
```

`cat number.txt`
```
767
352
842
963
```

`paste name.txt number.txt`
```
Ann       767
Martha    352
Jacob     842
George    963
```

`paste -d , name.txt number.txt `
```
Ann,767
Martha,352
Jacob,842
George,963
```

`paste -s name.txt number.txt`
```
Ann   Martha  Jacob  George
767   352     842    963
```
