give_me_pdf:
	npx @marp-team/marp-cli@latest slides.md --html --allow-local-files -o slides.pdf

convert_img:
	rm -f img/decision_tree.png && \
	pdftoppm -png img/decision_tree.pdf img/decision_tree
