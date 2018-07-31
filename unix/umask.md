# [⬅ Back	to Unix commands](unix.md)
# `umask`
Get or set the file creation mask (which controls how file permissions are set for newly created files)

`umask` display the current mask using octal notation, e.g.
>0022

`umask -S` display the current mask using symbolic notation, e.g.
>u=rwx,g=rx,o=rx

`umask <mode>` set the mask to &lt;mode&gt;, where &lt;mode&gt; can be expressed using octal or symbolic notation (like in [`chmod`](chmod.md) command), e.g.
 - `umask u+w,go-w` allow write permission to be enabled for the owner; prohibit write permission from being enabled for the group and others
 - `umask 077` allow read, write, and execute permission for the file's owner, but prohibit read, write, and execute permission for everyone else
