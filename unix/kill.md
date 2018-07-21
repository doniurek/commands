# [⬅ Back	to Unix commands](unix.md)
# `kill`
Send a signal to a process. By default, the message sent is the termination signal (SIGTERM).

## Options
`-l` List signal names.

`-s` or `-<signal>` Specify the signal to be sent. The signal can be specified by using name or number.
* `SIGTERM` request process termiantion. Unlike the SIGKILL signal, it can be caught and interpreted or ignored by the process. This allows the process to perform nice termination releasing resources and saving state if appropriate
* `SIGKILL` or `-9` cause process to terminate immediately (kill). In contrast to SIGTERM, this signal cannot be caught or ignored, and the receiving process cannot perform any clean-up upon receiving this signal.

## Comments
Use this command carefully and only if you really have to.
