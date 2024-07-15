.POSIX:
.SUFFIXES:
.PHONY: all clean install check
all:
PROJECT=flycheck
VERSION=1.0.0
PREFIX=/usr/local

all:
clean:
install:
check:
## -- BLOCK:license --
install: install-license
install-license: 
	mkdir -p $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
	cp COPYING $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
## -- BLOCK:license --
## -- BLOCK:sh --
install: install-sh
install-sh:
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	cp bin/chk              $(DESTDIR)$(PREFIX)/bin
	cp bin/chk-flags        $(DESTDIR)$(PREFIX)/bin
	cp bin/chk-h-emacs      $(DESTDIR)$(PREFIX)/bin
	cp bin/flytags          $(DESTDIR)$(PREFIX)/bin
## -- BLOCK:sh --
