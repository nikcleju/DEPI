
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
PANDOC_OPTIONS = -f markdown+latex_macros+backtick_code_blocks+raw_attribute --standalone -t beamer --slide-level 3 --include-in-header macros.md

# PWeave options
PWEAVE = pweave
PWEAVE_OPTIONS = -f pandoc
PWEAVE_OPTIONS_FAST = -f pandoc --documentation-mode

# Other options
RM=/bin/rm


# Make Rules

# slides_header needed at start, otherwise needs a level-1 header
%.pdf : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ slides_header.md $<

%.odt : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ slides_header.md $<

%.tex : %.md
	$(PANDOC) $(PANDOC_OPTIONS) -o $@ slides_header.md $<

%.md : %.mdw
ifeq ($(PWEAVE_FAST),TRUE)
	echo "Skipping Pweave regeneration of images"
	$(PWEAVE) $(PWEAVE_OPTIONS_FAST) -o $@ $<
else
	$(PWEAVE) $(PWEAVE_OPTIONS) -o $@ $<
endif

# What is this?
.PHONY: all clean

all : pdf

debug : tex pdf

odt : $(EXPORTED_DOCS_ODT)

pdf : $(EXPORTED_DOCS_PDF)

tex : $(EXPORTED_DOCS_TEX)

md : $(EXPORTED_DOCS_MD)

clean:
	- $(RM) $(EXPORTED_DOCS_PDF)
	- $(RM) $(EXPORTED_DOCS_ODT)
	- $(RM) $(EXPORTED_DOCS_TEX)
	- $(RM) $(EXPORTED_DOCS_MD)
