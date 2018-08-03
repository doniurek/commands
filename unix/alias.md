# [⬅ Back	to Unix commands](unix.md)
# `alias`
Define or display aliases

## Examples
`alias smile='echo ":)"'`
then if you type `smile` the output is:
```
:)
```

`alias`
```
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias grep='grep --color=auto'
alias l='ls -CF'
alias la='ls -A'
alias ll='ls -alF'
alias ls='ls --color=auto'
```

## Comments
Aliases disappears after ending terminal session
