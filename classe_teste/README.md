

# Estrutura dos arquivos

```sh
README.md  # Manual dos arquivos
LIVRO.tex  # Preâmbulos (classe, pacotes, comandos exporáticos; referência a outros arquivos)
	 |
	INPUTS.tex
		 |
		1.fronte.tex       		# [Frontistício]
		2-creditos.tex     		# [Créditos]
		3-rosto.tex     		# [folha de rosto]
		ARQUIVO_DE_TEXTO_A.tex		# Qualquer arquivo
		ARQUIVO_DE_TEXTO_B.tex
		ARQUIVO_DE_TEXTO_C.tex
		ARQUIVO_DE_TEXTO_D.tex
		[MUSSUMIPSUM.tex]		# Arquivo LIPSUM genérico 
		Y-Publicidade.tex	   	# [lista de livros publicados]
		Z-Colofon.tex   		# [colofon]

image.png		# imagem modelo
edlab-extra.sty 	# miscelânia de comandos e ajustes
edlab-footnotes.sty	# definições sobre notas
edlab-git.sty		# falso pacote .sty. arquivo temporário para guardar git ID
edlab-margins.sty	# dimensões do livro
edlab-penalties		# penalidades para ajustes da mancha de texto
edlab-sections.sty	# formatação de seções e cabeço
edlab-toc.sty		# formatação do sumário
Makefile 		# atalhos de comando. Ex: make; make clean
.gitignore 		# lista de arquivos ou tipos de arquivos que não vão subir para o github
gitrevisioninfo.sty 	# arquivo criado automaticamente com o número do git
```

# Vídeos

## Tópico: LaTeX: Formatações básicas (memoir)
```
Data: 30 abr. 2021 12:13 da tarde São Paulo

Gravação da reunião:
https://us02web.zoom.us/rec/share/m2gXTRsFztetm_gNDZxRDvDVBRzhwsfPY-gkaANlL_cItw_5oIVAvfuWOk50KzON.7J_RWMmOxC_KzXrP

Senha de acesso: !!!LaTeX!!13
```

## Topic: LaTeX: Estruturando arquivos
```
Start Time : May 5, 2021 03:03 PM

Meeting Recording:
https://us02web.zoom.us/rec/share/XtPWr6SFd7RqY5HHb6G3j9UOm7aflMXc8gXEEWYYF7jEgM3grFpFI3rOpNQzHO4R.fqfsZGudCtkACdUN

Access Passcode: !!!LaTeX13!!
```

## Topic: LaTeX: Partes do livro; Entendendo arquivos
```
Date: May 7, 2021 12:28 PM Sao Paulo

Meeting Recording:
https://us02web.zoom.us/rec/share/N0OXQujQ2-Pso_AfLFK1pBkqPQcISqC1Pa7BMvD2OfKlS8sWKcyTmuCZOuLWCtM6.2aaCN4-f1xeHPQDX

Access Passcode: !!!LaTeT!!13
```

## Topic: LaTeX: Apresentação da Nova Classe EdLab
```
Date: May 10, 2021 12:47 PM Sao Paulo

Meeting Recording:
https://us02web.zoom.us/rec/share/CMw7woaCMesZXFTMoQtO4iCtPvs9VLvyo79kROFnSUnzz0agAJHx9DXNv3vcn1S8.yPsNtIJlTm3ssjFs

Access Passcode: !!!LaTeX!!13
```

----

## Tips

```sh
# Remove os links internos e fixa \part como a primeira categoria de seções
$ pandoc -r markdown-auto_identifiers -w latex --top-level-division=part A.md -o A.tex
```

