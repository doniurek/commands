# [⬅ Back	to Unix commands](unix.md)
# `lp`
Send files to a printer

## Options
`-U <username>` Specifies the username to use when connecting to the server.

`-d` <printer_name> Prints files to the named printer

`-n <copies>` Set the number of copies to print

`-P <page_list>` Specifies which pages to print in the document. The list can contain a list of numbers and ranges separated by commas, e.g., "1,3-5,16". The page numbers refer to the output pages and not the document's original pages - options like `-o number-up` can affect the numbering of the pages.

### Common job options
`-o media=<size>` Sets  the  page size to &lt;size&gt;. Most printers support at least the size names "a4", "letter", and "legal".

`-o orientation-requested=4` Prints the job in landscape (rotated 90 degrees).

`-o sides=one-sided` Prints on one side of the paper.

`-o sides=two-sided-long-edge` Prints on both sides of the paper for portrait output.

`-o sides=two-sided-short-edge` Prints on both sides of the paper for landscape output.

`-o fit-to-page` Scales the print file to fit on the page.

`-o number-up=<2/4/6/9/16>` Prints 2, 4, 6, 9, or 16 document (input) pages on each output page.
