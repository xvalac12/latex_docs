BASH = /usr/bin/env bash
PROJ = proj5

all:
	latex $(PROJ).tex
	latex $(PROJ).tex
	dvips $(PROJ).dvi
	ps2pdf  $(PROJ).ps

zip:
	zip xvalac12-fit.zip proj5.tex Makefile

clean:
	rm -f $(PROJ).{aux,dvi,log,pdf,ps,out,vrb,toc,snm,nav} xvalac12-fit.zip
