# [⬅ Back	to Unix commands](Unix.md)
# `cat`
Concatenate and print files

## Options
`-b` number nonempty output lines
`-n` number all output lines

## Examples
`cat Desktop/test.txt`
>Alo? Salut! Sunt eu, un haiduc
şi te rog iubirea mea primeşte, fericirea
Alo? Alo! Sunt eu, Picasso.
Ţi-am dat beep şi sunt voinic
dar să ştii nu-ţi cer nimic.

>Vrei să pleci dar
nu mă, nu mă iei,
nu mă, nu mă iei,
nu mă, nu mă, nu mă iei.
Chipul tău şi
dragostea din tei
mi-amintesc de ochii tăi.


`cat -b Desktop/test.txt`
> 1	Alo? Salut! Sunt eu, un haiduc
     2	şi te rog iubirea mea primeşte, fericirea
     3	Alo? Alo! Sunt eu, Picasso.
     4	Ţi-am dat beep şi sunt voinic
     5	dar să ştii nu-ţi cer nimic.

  >   6	Vrei să pleci dar
     7	nu mă, nu mă iei,
     8	nu mă, nu mă iei,
     9	nu mă, nu mă, nu mă iei.
    10	Chipul tău şi
    11	dragostea din tei
    12	mi-amintesc de ochii tăi.


`cat -n Desktop/test.txt`
>   1	Alo? Salut! Sunt eu, un haiduc
     2	şi te rog iubirea mea primeşte, fericirea
     3	Alo? Alo! Sunt eu, Picasso.
     4	Ţi-am dat beep şi sunt voinic
     5	dar să ştii nu-ţi cer nimic.
     6
     7	Vrei să pleci dar
     8	nu mă, nu mă iei,
     9	nu mă, nu mă iei,
    10	nu mă, nu mă, nu mă iei.
    11	Chipul tău şi
    12	dragostea din tei
    13	mi-amintesc de ochii tăi.
