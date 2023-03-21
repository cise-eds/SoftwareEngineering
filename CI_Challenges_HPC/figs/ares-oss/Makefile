#
# Graphs for SI
#

TARGETS = ares-tricolor.pdf ares-tricolor-legend.pdf
CPP = cpp

all: $(TARGETS)

%.dot: %.dot.in
	cpp -P $< > $@

%.pdf: %.dot
	dot -Tpdf < $< > $@
	pdfcrop $@ $@.cropped.pdf
	mv $@.cropped.pdf $@

clean:
	rm -f $(TARGETS) *.dot
