# If the bib problem appears with 
# 'Bibliography not compatible with author-year citations.'
# just change the main.tex natbib option authoryear for numbers, 
# run it once, make it work, then go back to its original state. done
#
CURRENTDIR=`pwd`

all:	fmt-pdf fmt-rtf

fmt-pdf:
	pdflatex main
	bibtex main
	makeindex main.glo -s main.ist -t main.glg -o main.gls
	pdflatex main
	pdflatex main	
fmt-rtf:
	cp img/* . 
	latex2rtf -o timoteoPonce_frameworkDCI.rtf main.tex
	mv main.pdf timoteoPonce_frameworkDCI.pdf
	rm -rf *.aux *.log *.png *.eps *.out *.dvi *.tmp *.idv *.4ct *.4tc *.gls *.backup *.glg *.lof *.4og *.ist *.lot *.toc *.lof *.xref *.lg
clean:
	rm -rf *.aux *.log *.png *.eps *.out *.dvi *.tmp *.idv *.4ct *.4tc *.gls *.backup *.glg *.lof *.4og *.ist *.lot *.toc *.lof *.pdf *.lg *.xref 
	#rm -rf output
	#mkdir output
