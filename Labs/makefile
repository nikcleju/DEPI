
# Source md filenames, excluding macros.md and slides_header.md
SOURCE_MD = $(filter-out macros.md slides_header.md, $(wildcard *.md))

# Source mdw filenames
SOURCE_MDW = $(wildcard *.mdw)

# Exported md filenames
EXPORTED_DOCS_MD = $(SOURCE_MDW:.mdw=.md)

# Exported pdf filenames
EXPORTED_DOCS_PDF = $(SOURCE_MD:.md=.pdf)

# Exported odt filenames
EXPORTED_DOCS_ODT = $(SOURCE_MD:.md=.odt)

# Exported tex filenames
EXPORTED_DOCS_TEX = $(SOURCE_MD:.md=.tex)


# Pandoc options
PANDOC = pandoc
PANDOC_OPTIONS = -f markdown+latex_macros --standalone 

# PWeave options
PWEAVE = pweave
PWEAVE_OPTIONS = -f pandoc

# Other options
RM=/bin/rm


# Make Rules

%.pdf : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ $<

%.odt : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ $<

%.tex : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ $<

%.md : %.mdw
	$(PWEAVE) $(PWEAVE_OPTIONS) -o $@ $<

# What is this?
.PHONY: all clean

all : tex odt pdf

odt : $(EXPORTED_DOCS_ODT)

pdf : $(EXPORTED_DOCS_PDF)

tex : $(EXPORTED_DOCS_TEX)

md : $(EXPORTED_DOCS_MD)

clean:
	- $(RM) $(EXPORTED_DOCS_PDF)
	- $(RM) $(EXPORTED_DOCS_ODT)
	- $(RM) $(EXPORTED_DOCS_TEX)
	- $(RM) $(EXPORTED_DOCS_MD)
