build:	$(SOURCE)
	#cp -v -f ../localmetadata.tex localmetadata.tex
	xelatex --interaction=batchmode main; \
	cp -v -f ../lengths.tex lengths.tex
	xelatex --interaction=batchmode main; \
	mv main.pdf neue.pdf; \
	qpdf ../createspace/createspacecontent.pdf --pages ../createspace/createspacecontent.pdf 1-3 neue.pdf 4 ../createspace/createspacecontent.pdf 5-z -- output.pdf; \
	mv output.pdf ../createspace/educontent.pdf;\
	make clean
	xelatex cover; xelatex cover;\
	mv cover.pdf ../createspace/educover.pdf;\
	make clean;

clean:
	rm -f *.bak *~ *.backup *.tmp \
	*.adx *.and *.idx *.ind *.ldx *.lnd *.sdx *.snd *.rdx *.rnd *.wdx *.wnd \
	*.log *.blg *.ilg \
	*.aux *.toc *.cut *.out *.tpm *.bbl *-blx.bib *_tmp.bib \
	*.glg *.glo *.gls *.wrd *.wdv *.xdv \
	*.run.xml

