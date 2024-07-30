# Makefile for LaTeX project

# The main tex file
MAIN = acmc-template

# LaTeX compiler
LATEX = pdflatex

# BibTeX compiler
BIBTEX = bibtex

# Default target
all: $(MAIN).pdf

# Rule to make the PDF
$(MAIN).pdf: $(MAIN).tex
	$(LATEX) $(MAIN)
	$(BIBTEX) $(MAIN)
	$(LATEX) $(MAIN)
	$(LATEX) $(MAIN)

# Clean up auxiliary files
clean:
	rm -f $(MAIN).aux $(MAIN).log $(MAIN).out $(MAIN).toc \
		$(MAIN).bbl $(MAIN).blg $(MAIN).synctex.gz

# Clean up everything including the PDF
distclean: clean
	rm -f $(MAIN).pdf

# Phony targets
.PHONY: all clean distclean