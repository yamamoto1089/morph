# Process this file with automake to produce Makefile.in

man_MANS = cabocha.1
EXTRA_DIST = $(man_MANS)

update-man:
	@for man in $(man_MANS); do \
		cmd=`basename $$man .1` && \
		LANG=C help2man --no-info ../src/$$cmd | \
		perl -pe s/\\bFSF\\b/CaboCha/  | \
		perl -pe 's/(LT|lt)-//g' > $$man; \
	done
