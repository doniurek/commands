# [⬅ Back	to Unix commands](unix.md)
# `tr`
Translate or delete characters

`tr <set1> [set2]`

## Options
`-c` use the complement of &lt;set1&gt;

`-d` delete characters in &lt;set1&gt;

`-s` replace  each  sequence of a repeated character that is listed in the last specified &lt;set1&gt;, with a single occurrence of that character

`-s` first truncate &lt;set1&gt; to length of &lt;set2&gt;

## Example
`tr -d 'ek'`
open interactive session

`Cheeki Breeki`
```
Chi Bri
```

`tr -s 'ae'`
open interactive session

`yeeeaaah boiiiiii`
```
yeah boiiiiii
```

`tr 'lo' 'ke'`
open interactive session

`lol`
```
kek
```

`tr 'abcdef' 'xyz'`\
`abcdef`
```
xyzzzz
```

`tr -t 'abcdef' 'xyz'`\
`abcdef`
```
xyzdef
```

`tr -cd '[:alnum:]'` removes all non-alphanumeric characters

`echo "Bobby 175" | tr b m | tr -d [:digit:]`
```
Mommy
```

## Comments
Sets can be *POSIX* characters sets such as [:alnum:]. Full list of interpreted sequences is available on `tr` manual.
