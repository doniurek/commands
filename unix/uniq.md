# [⬅ Back	to Unix commands](unix.md)
# `uniq`
Report or omit repeated lines

Filter  adjacent  matching  lines from &lt;input&gt; (or standard input), writing to &lt;output&gt; (or standard output)

## Options
`-c` prefix lines by the number of occurrences

`-i` ignore differences in case when comparing

`-u` only print unique lines

## Example
`cat badger.txt`
```
Badger
badger
badger
badger
badger
badger
badger
badger
badger
badger
Mushroom
mushroom
a
Badger
badger
badger
badger
badger
badger
badger
badger
badger
badger
Mushroom
mushroom
a
Badger
badger
badger
badger
badger
badger
badger
badger
badger
badger
Mush-mushroom
a
Badger
badger
badger
badger
badger
badger
badger
badger
badger
badger
African!Snake
asnake
Snake!Asnake
oohit'sasnake
```

`uniq -c badger2.txt`
```
1 Badger
9 badger
1 Mushroom
1 mushroom
1 a
1 Badger
9 badger
1 Mushroom
1 mushroom
1 a
1 Badger
9 badger
1 Mush-mushroom
1 a
1 Badger
9 badger
1 African! Snake
1 a snake
1 Snake! A snake
1 ooh it's a snake

```

`sort badger2.txt | uniq -i`
```
a
African! Snake
a snake
badger
Mush-mushroom
mushroom
ooh it's a snake
Snake! A snake
```
