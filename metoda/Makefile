SRC=metoda.tex literatura.tex fdl.tex part1.tex part2.tex part3.tex part4.tex part5.tex part6.tex part7.tex part8.tex part9.tex part10.tex part11.tex
DEST=metoda.dvi
HTMLKEYS=-charset utf8 -exec /bin/date
HTMLBZIP=metoda-html.tar.bz2

all: $(DEST)

$(DEST): $(SRC) 
	xelatex metoda.tex
	xelatex metoda.tex

pdf: metoda.pdf

metoda.pdf: $(DEST)
	dvipdft -p a5 -o $@ $(DEST) 

clean:
	@rm -f *.aux *.log *.toc *.dvi
 
bzip2: clean
	cd .. ;\
	tar -cjf metoda-src.tar.bz2 src;\
	tar -cjf metoda-html.tar.bz2 metoda-html
	
html: all
	hevea $(HTMLKEYS) -o metoda.html metoda.tex
#	latex2html -split +0 -html_version=3.2,i18n -iso_language RU.RU -no_images metoda.tex
	

		
