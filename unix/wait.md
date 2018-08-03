# [⬅ Back	to Unix commands](unix.md)
# `wait`
Suspend execution of the calling process until one of its children (background process) terminates

`wait <process_id>`

## Examples
`sleep 60 &`
```
[2] 10066
```

`wait 10066; exit`\
in effect `exit` will take place after the termination of background process (10066)

`&` written after command runs this command in the background and return its PID\
`;` separates distinct commands (faciliates writing two commands in the same line)

## Comment
This command can be useful e.g. if you want to suspend termination of a program until the terminations of its subprograms
