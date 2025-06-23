BASH = /usr/bin/env bash
PROJ = proj3

all:
	latex $(PROJ).tex
	latex $(PROJ).tex
	dvips -t a4 $(PROJ).dvi
	ps2pdf -sPAPERSIZE=a4 $(PROJ).ps

zip:
	zip xvalac12-fit.zip *.eps *.tex algorithm2e.sty Makefile

clean:
	rm -f $(PROJ).{aux,dvi,log,pdf,ps,out} xvalac12-fit.zip
