# Reference Schemes

Here I describe the current (not desired) state as the starting point for discussion about what the general conventions should be.

## Apostolic Fathers

* Separate works are in separate files.
* Filenames are prefixed with a three-digit number and so are sortable.
* Each addressable textpart leaf is on its own line.
* The first token before whitespace is a reference for that textpart unique within the file.
* There is no indication in the reference of which of the 15 texts we are in (you need to know the filename for that)
* The hierarchy of textparts is expressed through a dotted notation (e.g. `3.2`)
* The references generally follow the standard referencing in the printed Lake.
* The components of the reference need not be numbers (e.g. 1 Clement ends with `SB.1`)
* The references should not be assumed to be sortable so the ordering of the lines is important
* All references have the same number of components (and therefore dots)
* Section headings often use `.0` (or `.0.0` in the case of Shepherd)

## MorphGNT

* Separate books are in separate files.
* Filenames are prefixed with a two-digit number (based on the SBLGNT source) and so are sortable.
* Each token (with punctuation included on the word token) is on its own line with addition token properties in different whitespace-delimited columns.
* The first column is a six-digit BBCCVV (e.g. 040316; so the reference does include the book).
* The CCVV part of the reference follows the standard chapter-verse scheme in the SBLGNT text.
* References are sortable although the files are not because there's no token-specific part of the reference

Of course, there *could* be a token-specific part of the reference.

## Vocabulary-Tools GNT

This is an alternative format of the MorphGNT data. See <https://github.com/jtauber/vocabulary-tools/tree/master/gnt_data> for more detail.

* Multiple alternative reference schemes are supported.
* The token data is in its own file (single file for whole GNT), one token per line with a token ID in the first column.
* A separate file for each of books, chapters, verses, sentences, paragraphs, and pericopes maps a different reference scheme to start and end token IDs (e.g. `verses.txt` has lines like `640316 50577 50601` which means verse `640316` (John 3.16) consists of tokens `50577` to `50601` inclusive).

## Enchiridion

* a single file
* Each section is on its own line (with a blank line between sections) other than `52` which has significant line breaks.
* Sub-sections are marked off with bracketed numberals like `[2]` within the running text of the section line
* There is an initial heading line.

Other than dealing with `52`, it would be trivial to convert this to the same format as the Apostolic Fathers.

## Perseus and OGL First1K Greek Files

* TEI XML following EpiDoc conventions
* directory layout follows Capitains Guidlines
* references are defined in a refsDecls section then inferred from the XML hierarchy based on regexes and XPath

## Sleeptillseven LXX

* like AF but including book name and with different delimiter character: `Genesis::1:1`
* Filenames are not sortable.
* References are not sortable.

## Nathans LXX

* like MorphGNT, token-per-line with whitespace-delimited columns (although BBCCCVVV for references)
* Filenames are prefixed with a two-digit number so are sortable.
