TEXOPTIONS=--lualatex --halt-on-error --interaction=nonstopmode --shell-escape --output-directory=build

all: build/packaging.pdf


build/packaging.pdf: FORCE | build
	max_print_line=1048576 \
	TEXINPUTS=../../.tex:../../.tex/beamertheme-vertex: \
	latexmk $(TEXOPTIONS) packaging.tex


preview: FORCE | build
	max_print_line=1048576 \
	TEXINPUTS=../../.tex:../../.tex/beamertheme-vertex: \
	latexmk -pvc $(TEXOPTIONS) packaging.tex

build:
	mkdir -p build

clean:
	rm -rf build

FORCE:


.PHONY: all clean FORCE
