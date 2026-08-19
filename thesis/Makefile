.PHONY: all
all: phd-thesis.pdf

%.pdf: FORCE
	@latexmk -pdf -pdflatex="pdflatex -interaction nonstopmode" -shell-escape -use-make $(basename $@)

FORCE:

.PHONY: clean
clean:
	@latexmk -C

.PHONY: clean-bib
clean-bib:
	@bibtool -r biblatex -s -i phd-thesis.bib -o phd-thesis.bib -- 'preserve.key.case = on' -- 'delete.field{abstract file}'
