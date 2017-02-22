# Add your language file here:
TARGETS = project.html

# Sciezki w Ubuntu
XSLTPROC = /usr/bin/xsltproc
XSL = /usr/share/xml/docbook/stylesheet/nwalsh/xhtml/docbook.xsl
#XSL = /usr/share/xml/docbook/stylesheet/nwalsh/xhtml/chunk.xsl

# Sciezki w Fedorze:
#XSLTPROC = /usr/bin/xsltproc
#XSL = /usr/share/sgml/docbook/xsl-stylesheets-1.73.2/xhtml/docbook.xsl
#XSL = /usr/share/sgml/docbook/xsl-stylesheets-1.73.2/xhtml/chunk.xsl

%.html: %.xml $(XSL)
	@$(XSLTPROC) --stringparam html.stylesheet.type text/css --stringparam html.stylesheet ede.css -o $@ $(XSL) $<

all: $(TARGETS)

clean:
	@rm -f *.html
