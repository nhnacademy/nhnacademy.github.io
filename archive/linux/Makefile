# jupyter nbconvert $< --to markdown --NbConvertApp.output_files_dir=.
.SUFFIXES: .ipynb .md .pdf

nb2md=nb2md
md2pdf=md2pdf

.ipynb.md:
	./$(nb2md) $<

.md.pdf:
	./$(md2pdf) $<

notebooks = $(wildcard *.ipynb)
mds = $(notebooks:%.ipynb=%.md)
pdfs = $(notebooks:%.ipynb=%.pdf)
md_files=$(notebooks:%.ipynb=%_files)
tex_header_file=header_file.tex

md: $(mds) $(nb2md)

pdf: $(pdfs) $(tex_header_file) $(md2pdf)

clean:
	rm -rf $(mds) $(md_files)

realclean: clean
	rm -rf $(pdfs)
