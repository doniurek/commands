# [⬅ Back	to Unix commands](unix.md)
# `rmdir`
Remove directories if they are empty

`rmdir <directory(ies)>`

## Options
`--ignore-fail-on-non-empty` do not prompt information about failure that is solely because a directory is non-empty

`-p` remove &lt;directory&gt; and its ancestors; e.g., `rmdir -p a/b/c` is similar to `rmdir a/b/c a/b a`

`-v` output a diagnostic for every directory processed
