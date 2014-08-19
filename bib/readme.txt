This directory includes a bibtex file exported by Matt from his Mendeley library that includes CISM-related references.

To update:
1. update the cism_bib.bib file or have Matt update it.

2. regenerate the html using one of these methods:
a) bibtex2html
Code can be downloaded from: https://www.lri.fr/~filliatr/bibtex2html/  including Mac binaries
If using Mac binaries, they need to be added to your path.
Also note: Note for Mac OSX users: TeXlive 2010 prevents bibtex2html to run bibtex in a temporary directory, resulting in an error message.
A workaround consists in telling bibtex2html to use the current directory for temporary files, using the following shell command before running bibtex2html:
  export TMPDIR=.
There are lots of command line options, but these are the options I used:
> bibtex2html --sort-by-date --reverse-sort --nodoc --nobibsource --no-abstract --no-keywords cism_bib.bib

b) PANDOC
Create an html page from the bibtex file using:
> pandoc get_bib_refs_using_pandoc.tex -o output.html --bibliography cism_bib.bib
Only the newest version of pandoc, which is not available yet on Macports can convert all references without specifying them all individually.  So I did not end up using this method, but leave it here for posterity.

3. Once the html is generated, manually paste it into the publications.html file in the main directory.

4. Commit your changes to cism_bib.bib and publications.html
