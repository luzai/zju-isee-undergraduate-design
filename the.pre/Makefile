main:
	xelatex -synctex=1 -interaction=nonstopmode -halt-on-error main
	biber main
	xelatex -synctex=1 -interaction=nonstopmode -halt-on-error main
	xelatex -synctex=1 -interaction=nonstopmode -halt-on-error main
	# cp main.pdf proposal.xinglu.pdf
clean:
	# git clean -dfX
	rm -rf *.nav *.toc *.aux *.log *.snm *.out

watch: main.tex data/kaitibaogao.tex data/kaitibaogao.bib data/waiwenfanyi.tex data/kaohe.tex data/yaoqiu.tex
	fswatch -o $^ | xargs -n1 -I{} make