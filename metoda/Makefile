SRC=metoda.tex literatura.tex part1.tex part2.tex part3.tex part4.tex part5.tex part6.tex part7.tex part8.tex part9.tex part10.tex
DEST=metoda.dvi
HTMLKEYS=-charset cp1251 -exec /bin/date
HTMLBZIP=metoda-html.tar.bz2

all: $(DEST)

$(DEST): *.tex 
	texi2dvi metoda.tex

pdf: metoda.pdf

metoda.pdf:
	dvipdf $(DEST) $@

clean:
	@rm -f *.aux *.log *.toc *.dvi
 
bzip2: clean
	cd .. ;\
	tar -cjf metoda-src.tar.bz2 src;\
	tar -cjf metoda-html.tar.bz2 metoda-html
	
html: all
	hevea $(HTMLKEYS) -o ../metoda.html metoda.tex
	

		
