main:
	# latexmk -xelatex main
	xelatex  -interaction=nonstopmode -halt-on-error main
	bibtex main
	xelatex  -interaction=nonstopmode -halt-on-error main
	xelatex  -interaction=nonstopmode -halt-on-error main

clean:
	git clean -dfX

watch: main.tex data/kaitibaogao.tex data/kaitibaogao.bib data/waiwenfanyi.tex data/kaohe.tex data/yaoqiu.tex
	fswatch -o $^ | xargs -n1 -I{} make