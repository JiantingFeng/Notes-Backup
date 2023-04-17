all: main.pdf

.PHONY: format clean

COMPILER = pdflatex
BIB = bibtex
INDENTER = latexindent

format:
	$(INDENTER) -w main.tex

main.pdf: format
	$(COMPILER) main.tex
	$(BIB) main
	$(COMPILER) main.tex
	$(COMPILER) main.tex

clean:
	rm -f *.aux *.log *.bbl *.blg \
	 	*.bcf *.ind *.lof *.lot *.out *.toc \
	    *.acn *.acr *.alg *.glg *.glo *.gls *.ist \
	    *.fls *.fdb_latexmk *.nav *.snm \
	    *.synctex.gz *.run.xml *.bak*
