###############################################
#           build options                     #
###############################################
#
####### Building fetch support ################
#
#

SHELL=/bin/bash
DESTDIR=
BINDIR=${DESTDIR}/usr/bin
INFODIR=${DESTDIR}/usr/share/doc/fetch
SHAREDIR=${DESTDIR}/usr/share/fetch
MODE=775
DIRMODE=755

.PHONY: build

install:
	mkdir -p ${BINDIR}/
	install -m ${MODE} src/fetch ${BINDIR}/
	mkdir -p ${SHAREDIR}/
	install -m ${MODE} src/core.sh ${SHAREDIR}/
	mkdir -p ${INFODIR}/
	cp ChangeLog INSTALL LICENSE MAINTAINERS README.md ${INFODIR}/
	@echo
	@echo "Software was installed in ${BINDIR}"

uninstall:
	rm ${BINDIR}/fetch
	@echo "Software was removed."
