# [⬅ Back	to Unix commands](unix.md)
# `env`
Set the environment for command invocation

It is used to either print a list of environment variables or run another utility in an altered environment without having to modify the currently existing environment. Using env, environment variables may be added or removed, and existing variables may be changed by assigning new values to them.

## Options
To print out a list of all environment variables, simply run env without any arguments.

`-u` <variable> remove variable from the environment

## Examples
`echo 'echo $HOME' > domek.sh`
`chmod +x domek.sh`
`./domek.sh`
```
/home/donia
```

`env HOME='/root' ./domek.sh`
```
/root
```

`./domek.sh`
```
/home/donia
```
