PYTHON ?= python2
BUILDDIR ?= ../build
INDEXFILE ?= ../index.html
BUILDSLIDE ?= buildSlide.py
BUILDINDEX ?= buildIndex.py

all: slides index

slides: $(patsubst %.html, $(BUILDDIR)/%.html, $(wildcard *.html))

$(BUILDDIR)/%.html: %.html Makefile slide.tmpl metadata.json
	@$(PYTHON) $(BUILDSLIDE) $< > $@
	@echo "done: " $<

index: Makefile index.tmpl metadata.json
	@$(PYTHON) $(BUILDINDEX) $(BUILDDIR) > $(INDEXFILE)
	@echo "done: " $@


local:
	@cd .. && $(PYTHON) -m SimpleHTTPServer 8080

clean:
	@rm -f $(BUILDDIR)/*.html $(INDEXFILE)
	@echo "done: cleanup"


.PHONY: all slides index local clean
