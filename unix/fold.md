# [⬅ Back	to Unix commands](unix.md)
# `fold`
Wrap each input line to fit in specified width

## Options
`-s` break at spaces

`-w <width>` use &lt;width&gt; columns instead of default 80

## Examples
`cat test.txt`
> Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Curabitur dignissim
venenatis pede. Quisque dui dui, ultricies ut, facilisis non, pulvinar non,
purus. Duis quis arcu a purus volutpat iaculis. Morbi id dui in diam ornare
dictum. Praesent consectetuer vehicula ipsum. Praesent tortor massa, congue et,
ornare in, posuere eget, pede.

`fold -w 30 test.txt` maximum 30 characters per line
> Lorem ipsum dolor sit amet, co

>nsectetuer adipiscing elit. Cu

> rabitur dignissim

>venenatis pede. Quisque dui du

>i, ultricies ut, facilisis non

>, pulvinar non,

>purus. Duis quis arcu a purus

>volutpat iaculis. Morbi id dui

> in diam ornare

>dictum. Praesent consectetuer

>vehicula ipsum. Praesent torto

>r massa, congue et,

>ornare in, posuere eget, pede.
