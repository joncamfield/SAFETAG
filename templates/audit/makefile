
build/report.md:
	@echo "Building markdown file from report."
	../../modules/markdown-pp/markdown-pp.py index.report.md ../../build/report.md
	@echo "Building html file from markdown report."
	pandoc  --variable=title:"SAFEETAG Report" \
		--toc --toc-depth=2 -s \
		--template=../../theme/html5.template \
		--to=html5 ../../build/report.md \
		--output=../../build/report.html
	@echo "Building pdf from html report."
	wkhtmltopdf --user-style-sheet ../../theme/core.css \
		--title "SAFETAG Report" \
		--disable-smart-shrinking  \
		--footer-center "Page [page] of [toPage]" \
		--header-right [doctitle] \
		--outline \
		--outline-depth 2 \
		../../build/report.html ../../build/report.pdf
