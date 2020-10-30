# latex-manuscript
Templates, exemples, tips and tricks for a smoother experiance with latex, most especialy for a PhD thesis manuscript


## How to use

The folder `these-lpp` includes all that is needed to start your PhD manuscript.

The idea is that it can be used as a working template to start quickly your manuscript, as well as a (quite) commented exemple in order to know how to performe certain Latex things.

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

the main reason for that is historic. In the furute version, it should be fixed.

### Directory Layout

In order to faciliate the writting experiance, we decided to:
- have one main file at the root of the projects
- have each chapter in the subfolder, along with its figure
- have the settings in another file

### Page Layout

The usual layout is the A4 format (210 x 297 mm).
However, this is more usual to print a manuscript in B5 format (175 x 250 mm).

To do so, once could juste shrink the A5 to B5, but this would chang the font size, the figure size, and so one. 
Hence, it is best to set the page geometry with `\geometry`, or `\newgeometry`.

#### Margins

It took us a long time to choos the margin. It accually depends on a lot of parameters. For exemple: is it a web version or a printed version, how many pages, what techonoly used to manufacture the book, etc.

The inner margin should be wider than the outer margin (that is only use to put a thumb). however, it is defficult to chose which.
That's why we settled with the simples values : 20mm everywhere.

To allow a Figure, or a table, to git in the margin, one can use 
```
\makebox[\textwidth][c]{\includegraphics[width=<extrawidth>]{<figurename>}}%
```
For instance, `extrawidth` can be `1.2\textwidth`.

## Digging into the Latex Settup

Most of the Latex packages used are imported in `./texfiles/settings.tex`.
There, a lot is going. Take the time to review the file. 

Most of the packages are commented.

# Get in touch

Please contact the Laboratory of Plasma Physics communication team for any questions, comments, or anything else.

