#
#  Makefile
#

URL = http://localhost:4000/

help:
	@echo
	@echo "  make serve     Run a development server."
	@echo "  make view      Open the dev page in the browser."
	@echo "  make edit      Open the project in Atom."
	@echo

serve:
	while :; do gitbook serve --watch; sleep 1; done

view:
	while ! curl -o /dev/null -s $(URL); do sleep 0.1; done
	open $(URL)

edit:
	atom .

book.pdf: book.json *.md
	gitbook pdf
