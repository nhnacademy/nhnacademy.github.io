.SUFFIXES: .ipynb .md
.ipynb.md:
	jupyter nbconvert $< --to markdown --NbConvertApp.output_files_dir=.

all: parameter.md
