# [⬅ Back	to Unix commands](unix.md)
# `printf`
Format and print data

`printf <format> <argument(s)>` print &lt;argument(s)&gt; according to &lt;format&gt;

&lt;format&gt; can contain *format specifiers*

## Example
`X=$RANDOM;printf "decimal notation: %d\nscientific notation: %e\n" $X $X`
```
decimal notation: 31871
scientific notation: 3,187100e+04
```

Double `$X` because there are two format specifiers (`%d` and `%e`) in &lt;format&gt;
