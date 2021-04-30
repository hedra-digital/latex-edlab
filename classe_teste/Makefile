all:
	latexmk -lualatex LIVRO.tex
	evince LIVRO.pdf
clean:
	-rm *aux *log *tui *toc *.4ct *.4tc *.html *.css *.dvi *.epub *.lg *.ncx *.xref *.tmp *.idv *.opf *.png  LIVRO.pdf *.fdb_latexmk *.fls
git:
	git add .
	git commit -m "mudança pequena"
	git push

fonts-update:
	fc-cache -f -v
