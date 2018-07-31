# [⬅ Back	to Unix commands](unix.md)
# `unexpand`
Convert spaces to tabs

Convert blanks in each &lt;file&gt; to tabs, writing to standard output.

## Options
`-a` convert all blanks, instead of just initial blanks

`--first-only` convert only leading sequences of blanks (overrides `-a`)

`-t <num>` have tabs &lt;num&gt; characters apart instead of 8 (enables `-a`)

`-t <list>` use comma separated &lt;list&gt; of tab positions (enables `-a`)

## Example
`cat test.txt`
```
        Freestyler
Rock the         microphone
```

`unexpand testun.txt | cat -T`
```
^IFreestyler
Rock the         microphone
```

`unexpand -a testun.txt | cat -T`
```
^IFreestyler
Rock the^I microphone
```
