# Incremental Quarto renders, run from this directory (or use make -C Labs).
# Make compares actual output timestamps with the QMD sources.
# Requires GNU Make 4.3+ for grouped multi-format targets.
# Examples:
#   make                     # HTML, PDF and notebook (current QMD formats)
#   make TO=pdf              # PDF only
#   make pdf                 # shortcut for PDF only
#   make -n                  # preview commands without rendering
#   make -B                  # force renders (e.g. after changing images)
#   make SOURCES=Lab3_NormalDistribution.qmd
# Override QUARTO for a particular environment, e.g. QUARTO=/path/to/quarto.
# Missing outputs are rebuilt automatically; asset changes require make -B.

.DEFAULT_GOAL := all

QUARTO ?= quarto
TO ?= all
SOURCES ?= $(wildcard *.qmd Ro/*.qmd)
CONFIG := $(wildcard _quarto.yml _quarto.yaml ../_quarto.yml ../_quarto.yaml)

.DELETE_ON_ERROR:

ifeq ($(TO),all)
OUTPUTS := $(foreach ext,html pdf ipynb,$(SOURCES:.qmd=.$(ext)))

# These three outputs come from one Quarto invocation, not three separate renders.
%.html %.pdf %.ipynb &: %.qmd Makefile $(CONFIG)
	$(QUARTO) render "$<" --to all
else
OUTPUTS := $(SOURCES:.qmd=.$(TO))

%.$(TO): %.qmd Makefile $(CONFIG)
	$(QUARTO) render "$<" --to "$(TO)"
endif

.PHONY: all pdf
all: $(OUTPUTS)

pdf:
	$(MAKE) TO=pdf all
