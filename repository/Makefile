# Add your language file here:
TARGETS = dokumentacja-book.html

# Sciezki w Ubuntu
XSLTPROC = /usr/bin/xsltproc
#XSL = /usr/share/xml/docbook/stylesheet/nwalsh/xhtml/docbook.xsl
XSL = /usr/share/xml/docbook/stylesheet/nwalsh/xhtml/chunk.xsl

# Sciezki w Fedorze:
#XSLTPROC = /usr/bin/xsltproc
#XSL = /usr/share/sgml/docbook/xsl-stylesheets-1.73.2/xhtml/docbook.xsl
#XSL = /usr/share/sgml/docbook/xsl-stylesheets-1.73.2/xhtml/chunk.xsl

%.html: %.xml $(XSL)
	@$(XSLTPROC) --xinclude --stringparam generate.toc "book toc,title chapter toc,title,figure,table,example,equation part toc,title" --stringparam label.from.part 1 --stringparam chunk.section.depth 0 --stringparam use.id.as.filename 1 --stringparam toc.max.depth 2 --stringparam toc.section.depth 8 --stringparam section.autolabel 1 --stringparam callout.graphics.number.limit 35 --stringparam html.stylesheet.type text/css --stringparam html.stylesheet ede.css -o ../output/$@ $(XSL) $<

all: $(TARGETS)

clean:
	@rm -f ../output/*.html

# Notatki
# --stringparam generate.division.figure.lot 0 --stringparam generate.division.example.lot 0 --stringparam generate.division.equation.lot 0 --stringparam generate.division.table.lot 0
# --stringparam chunk.separate.lots 1
# --stringparam generate.toc "book toc,title,figure,table,example,equation chapter toc,title part toc,title"
# --stringparam generate.section.toc.level 4