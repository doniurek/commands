# [⬅ Back	to Unix commands](unix.md)
# `unalias`
Remove alias definitions

`unalias -a` remove __all__ aliases

`unalias <name>` remove <name> alias

## Example
`alias smile='echo ":)"'`\
`smile`
```
:)
```

`unalias smile`\
`smile`
```
bash: smile: command not found
```
