###############################################
#           build options                     #
###############################################
#
####### Building clonedisk support ################
#
#

SHELL=/bin/bash
DESTDIR=
BINDIR=${DESTDIR}/usr/bin
INFODIR=${DESTDIR}/usr/share/doc/clonedisk
SHAREDIR=${DESTDIR}/usr/share/clonedisk
APPDIR=${DESTDIR}/usr/share/applications
MODE=775
DIRMODE=755

.PHONY: build

install:
	mkdir -p ${BINDIR}/
	install -m ${MODE} src/chili-clonedisk ${BINDIR}/
	mkdir -p ${SHAREDIR}/
	install -m ${MODE} src/core.sh ${SHAREDIR}/
	mkdir -p ${APPDIR}/
	install -m ${MODE} src/chili-clonedisk.desktop ${APPDIR}/
	mkdir -p ${INFODIR}/
	cp ChangeLog INSTALL LICENSE MAINTAINERS ${INFODIR}/
	@echo
	@echo "Software was installed in ${BINDIR}"

uninstall:
	rm ${BINDIR}/chili-clonedisk
	@echo "Software was removed."
