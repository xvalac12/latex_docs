BASH=/usr/bin/env bash
NAME=proj4

.PHONY: clean pack bibtex pdflatex
 
$(NAME).pdf: $(NAME).ps
	ps2pdf -sPAPERSIZE=a4 $(NAME).ps

$(NAME).ps: $(NAME).dvi
	dvips -t a4 $(NAME).dvi

$(NAME).dvi: $(NAME).tex
	latex $(NAME).tex
	make bibtex
	latex $(NAME).tex
	latex $(NAME).tex

bibtex: $(NAME).bib
	bibtex $(NAME)

pdflatex: $(NAME).tex
		pdflatex $(NAME).tex
		make bibtex
		pdflatex $(NAME).tex
		pdflatex $(NAME).tex

zip:
	zip xvalac12-fit.zip $(NAME).{tex,bib} bibstyle.bst Makefile

clean:
	rm -f $(NAME).{aux,dvi,log,pdf,ps,out,bbl,blg} xvalac12-fit.zip

