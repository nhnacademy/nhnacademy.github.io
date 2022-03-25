.SUFFIXES: .ipynb .md
.ipynb.md:
	jupyter nbconvert $< --to markdown --NbConvertApp.output_files_dir=.

sources = $(wildcard *.ipynb)
targets = $(sources:%.ipynb=%.md)

all: $(targets) 
