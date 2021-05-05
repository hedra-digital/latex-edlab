all:
	git log -1 --date=short --format=format:'\newcommand{\RevisionInfo}{%h}' > gitrevisioninfo.sty
	latexmk -lualatex LIVRO.tex   # compilador
	evince LIVRO.pdf			  # linux: leitor de PDF
	open   LIVRO.pdf              # mac: leitor PDF
clean:
	-rm *aux *log *tui *toc *.4ct *.4tc *.html *.css *.dvi *.epub *.lg *.ncx *.xref *.tmp *.idv *.opf  LIVRO.pdf *.fdb_latexmk *.fls
git:
	git add .
	git commit -m "mudança pequena"
	git push
fonts-update:
	fc-cache -f -v
qualquercoisa:
	echo "oioioi"
