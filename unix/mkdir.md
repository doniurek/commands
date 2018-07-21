# [⬅ Back	to Unix commands](unix.md)
# `mkdir`
Make directories

## Options
`-m <mode>` set file mode (as in [`chmod`](chmod.md))

`-p` no error if existing, make parent directories as needed

## Example
`mkdir -p a/b` will create directory **a** if it doesn't exist, then will create directory **b** inside directory **a**. If the given directory already exists, ignore the error.
