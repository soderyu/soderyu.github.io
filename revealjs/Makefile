MAIN=index

$(MAIN).html: $(MAIN).md
	pandoc -f markdown -sSt revealjs \
	--mathjax="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML" -o $@ $<

.PHONY: clean clean-all
clean-all: clean
	rm -v $(MAIN).html || true
clean:
	true
