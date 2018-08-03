# [⬅ Back	to Unix commands](unix.md)
# `iconv`
Convert text from one character encoding to another

`iconv -f <from-encoding> -t <to-encoding>`

## Options
`-l` List all known character set encodings

`-c` Silently discard characters that cannot be converted

`-t <to-encoding>//IGNORE` characters that cannot be converted are discarded and an error is printed after conversion

`-t <to-encoding>//TRANSLIT` characters being  converted are transliterated when needed and possible or replaced with a question mark when cannot be represented by characters from new encoding set

## Examples
`echo dużo $ mało € scheiße α | | iconv -f UTF-8 -t ASCII//TRANSLIT`
```
malo EUR sheisse ?
```

`echo dużo $ mało € scheiße α | | iconv -f UTF-8 -t ASCII//IGNORE`
```
mao  sheie
```
