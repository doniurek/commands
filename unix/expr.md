# [⬅ Back	to Unix commands](unix.md)
# `expr`
Evaluate arguments as an expression

## Examples
`1 \< 2`
```
bash: 1: command not found
```

`expr 1 \< 2`
```
1
```
What means - true

`expr 1 \> 2`
```
0
```
What means - false

## Comments
Beware that many operators need to be escaped (by \\) or quoted!
