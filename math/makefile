main : src/main.tex temp/main/main.aux temp/main/main.bbl temp/main/main.out temp/main/main.toc
	mv temp/main/main.aux src/main.aux
	mv temp/main/main.bbl src/main.bbl
	mv temp/main/main.out src/main.out
	mv temp/main/main.toc src/main.toc
	cd src && /mnt/c/texlive/2021/bin/win32/ptex2pdf.exe -l -u -halt-on-error main.tex
	mv src/main.aux temp/main/main.aux
	mv src/main.bbl temp/main/main.bbl
	mv src/main.log temp/main/main.log
	mv src/main.out temp/main/main.out
	mv src/main.toc temp/main/main.toc
	mv src/main.pdf main.pdf

bib : temp/main/main.aux
	mv temp/main/main.aux src/main.aux
	cd src && /mnt/c/texlive/2021/bin/win32/upbibtex.exe main
	mv src/main.aux temp/main/main.aux
	mv src/main.bbl temp/main/main.bbl
	mv src/main.blg temp/main/main.blg

mainbib : 
	make main
	make bib
	make main
	make main

intro : src/intro.tex temp/intro/intro.aux temp/intro/intro.out
	mv temp/intro/intro.aux src/intro.aux
	mv temp/intro/intro.out src/intro.out
	cd src && /mnt/c/texlive/2021/bin/win32/ptex2pdf.exe -l -u -halt-on-error intro.tex
	mv src/intro.aux temp/intro/intro.aux
	mv src/intro.log temp/intro/intro.log
	mv src/intro.out temp/intro/intro.out
	mv src/intro.pdf intro.pdf
