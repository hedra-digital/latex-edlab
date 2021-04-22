all:
	git log -1 --date=short --format=format:'\newcommand{\RevisionInfo}{%h}' > gitrevisioninfo.sty
	latexmk -lualatex LIVRO.tex


erros:
	-grep --color=auto "LaTeX Error" LIVRO.log
	-grep --color=auto -A 3 "Undefined" LIVRO.log

test:
	xelatex LIVRO.tex
	xelatex LIVRO.tex
	evince LIVRO.pdf

clean:
	-rm *aux *log *tui *toc *xdv *.4ct *.4tc *.html *.css *.dvi *.epub *.lg *.ncx *.xref *.tmp *.idv *.opf *.fls *_latexmk LIVRO.pdf
	-rm -rf EBOOK-epub
	-rm -rf EBOOK-epub3
	-rm -rf EBOOK-mobi

git:
	git add .
	git commit -m "direto na linha de comando"
	git push

# Manipulação de arquivos ##########################################################
rename:
	cp LIVRO.pdf $(TITULO)_MIOLO_$(GIT).pdf
clean_arquivosgerais:
	mv ~/Dropbox/ARQUIVOS_GERAIS/$(TITULO)_MIOLO_* ~/Dropbox/ARQUIVOS_GERAIS/OLD/
delivery:
	cp $(TITULO)_MIOLO_$(GIT).pdf ~/Dropbox/ARQUIVOS_GERAIS/
	echo $(GIT) '--- Entregue em' "$$(date)" >> ENTREGAS.txt

# Ebook                   ##########################################################
pandoc:
	mkdir -p ebook
	pandoc LIVRO.tex -o ./ebook/$(TITULO).epub
check:
	epubcheck ./ebook/$(TITULO).epub
sigil:
	sigil ./ebook/$(TITULO).epub
capa-internet:
	wget https://hedra.com.br/uploads/book/cover/$(INTERNET).${EXTENSAO}
	mv $(INTERNET).${EXTENSAO} ./ebook/$(COVER)
	mogrify -format png ./ebook/$(COVER)
capa:
	mogrify -resize x2550 ./ebook/capa.jpg
	mogrify -format png ./ebook/capa.jpg