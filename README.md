# latex-manuscript
Templates, exemples, tips and tricks for a smoother experiance with latex, most especialy for a PhD thesis manuscript


## How to use

The folder `these-lpp` includes all that is needed to start your PhD manuscript.

### How to compile


* Parse a first time the sources : `pdflatex -draftmode manuscript.tex`
* Generate the bibliography : `bibtex manuscript.aux`
* Generate the nomenclatires : `makeindex manuscript.nlo -s nomencl.ist -o manuscript.nls`
* Generate twice the pdf : `pdflatex manuscript.tex`

The one liner : 
```
pdflatex -draftmode manuscript.tex && bibtex manuscript.aux && makeindex manuscript.nlo -s nomencl.ist -o manuscript.nls && pdflatex manuscript.tex && pdflatex manuscript.tex
```

### Cover pages

The UPSaclay and IPP covers are included in the template.

THe UPSacaly cover pages are included directly into the file, while the IPParis pages have to be compiled separetely before beeing included as PDFs.

## Digging into the Latex Settup

Most of the Latex packages used are imported in `./texfiles/settings.tex`.
There, a lot is going. Take the time to review the file. 

Most of the packages are commented.

# Get in touch

Please contact the Laboratory of Plasma Physics communication team for any questions, comments, or anything else.

