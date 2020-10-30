# Exemple of a thesis manuscript

Addapted from Antoine Tavant's thesis


## How to compile


* Parse a first time the sources : `pdflatex -draftmode manuscript.tex`
* Generate the bibliography : `bibtex manuscript.aux`
* Generate the nomenclatires : `makeindex manuscript.nlo -s nomencl.ist -o manuscript.nls`
* Generate twice the pdf : `pdflatex manuscript.tex`

The one liner : 
```
pdflatex -draftmode manuscript.tex && bibtex manuscript.aux && makeindex manuscript.nlo -s nomencl.ist -o manuscript.nls && pdflatex manuscript.tex && pdflatex manuscript.tex
```
