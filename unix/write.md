# [⬅ Back	to Unix commands](unix.md)
# `write`
Send a message to another user's terminal

`write <user> [tty]`

When you run the write command, the user you are writing to gets a message of the form:
```
Message from yourname@yourhost on yourtty at hh:mm ...
```

Any further lines you enter will be copied to the specified user's terminal. If the other user wants to reply, they must run write as well.

When you are done, type an **end-of-file** or interrupt character (^C). The other user will see the message **EOF** indicating that the conversation is over.

## Examples
`write Ann`
```
write: donia is logged in more than once; writing to pts/0
```
`Hello Ann!`

This occurs on Ann's terminal (pts/0):
```
Message from Bob@work on pts/1 at 14:48 ...
Hello Ann!
```

Ann can response:
`write Bob`
```
write: donia is logged in more than once; writing to pts/1
```
`Hi Bob! How are you?`

And this occurs on Bob's terminal:
```
Message from Ann@work on pts/0 at 14:50 ...
Hi Bob! How are you?
```
