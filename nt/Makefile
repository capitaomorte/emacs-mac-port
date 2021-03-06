### nt/Makefile.  Generated from Makefile.in by configure.

# Copyright (C) 2013-2014 Free Software Foundation, Inc.

# This file is part of GNU Emacs.

# GNU Emacs is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.

# GNU Emacs is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.

# You should have received a copy of the GNU General Public License
# along with GNU Emacs.  If not, see <http://www.gnu.org/licenses/>.

# Avoid trouble on systems where the `SHELL' variable might be
# inherited from the environment.
SHELL = /bin/sh

# ==================== Things `configure' will edit ====================

CC=gcc
CFLAGS=-g3 -O2
version=24.3.92
## Used in $archlibdir.
configuration=x86_64-apple-darwin13.3.0
EXEEXT=
C_SWITCH_SYSTEM=
C_SWITCH_MACHINE=
PROFILING_CFLAGS = 
WARN_CFLAGS =  -Wno-switch -Wno-tautological-constant-out-of-range-compare -Wno-pointer-sign
WERROR_CFLAGS = 

# Program name transformation.
TRANSFORM = s,x,x,

# ==================== Where To Install Things ====================

# The default location for installation.  Everything is placed in
# subdirectories of this directory.  The default values for many of
# the variables below are expressed in terms of this one, so you may
# not need to change them.  This is set with the --prefix option to
# `../configure'.
prefix=/usr/local

# Like `prefix', but used for architecture-specific files.  This is
# set with the --exec-prefix option to `../configure'.
exec_prefix=${prefix}

# Where to install Emacs and other binaries that people will want to
# run directly (like etags).  This is set with the --bindir option
# to `../configure'.
bindir=${exec_prefix}/bin

# The root of the directory tree for read-only architecture-independent
# data files.  ${datadir}, ${infodir} and ${mandir} are based on this.
datarootdir=${prefix}/share

# Where to install architecture-independent data files.  ${lispdir}
# and ${etcdir} are subdirectories of this.  This is set with the
# --datadir option to `../configure'.
datadir=${datarootdir}

# Where to install and expect executable files to be run by Emacs
# rather than directly by users, and other architecture-dependent
# data.  ${archlibdir} is usually below this.  This is set with the
# --libexecdir option to `../configure'.
libexecdir=${exec_prefix}/libexec

# Directory for local state files for all programs.
localstatedir=${prefix}/var

# Where to find the source code.  This is set by the configure
# script's `--srcdir' option.  However, the value of ${srcdir} in
# this makefile is not identical to what was specified with --srcdir,
# since the variable here has `/lib-src' added at the end.

# We use $(srcdir) explicitly in dependencies so as not to depend on VPATH.
srcdir=.


# The top-level source directory, also set by configure.
top_srcdir=..
# MinGW CPPFLAGS may use this.
abs_top_srcdir=/Users/capitaomorte/Source/Emacs/emacs-mac-port-manual/emacs-24.3.92

# ==================== Emacs-specific directories ====================

# These variables hold the values Emacs will actually use.  They are
# based on the values of the standard Make variables above.

# Where to put executables to be run by Emacs rather than the user.
# This path usually includes the Emacs version and configuration name,
# so that multiple configurations for multiple versions of Emacs may
# be installed at once.  This can be set with the --archlibdir option
# to `../configure'.
archlibdir=${libexecdir}/emacs/${version}/${configuration}

# ==================== Utility Programs for the Build =================

# ../configure figures out the correct values for these.
INSTALL = /usr/bin/install -c
INSTALL_DATA = ${INSTALL} -m 644
INSTALL_PROGRAM = ${INSTALL}
INSTALL_SCRIPT = ${INSTALL}
# By default, we uphold the dignity of our programs.
INSTALL_STRIP =
MKDIR_P = ../build-aux/install-sh -c -d

# ========================== Lists of Files ===========================

# Things that a user might actually run, which should be installed in bindir.
INSTALLABLES = runemacs${EXEEXT} addpm${EXEEXT}

# Things that Emacs runs internally, which should not be installed in bindir.
UTILITIES = cmdproxy${EXEEXT} ddeclient${EXEEXT}

# Things that Emacs runs during the build process.
DONT_INSTALL = addsection${EXEEXT}

# All files that are created by the linker, i.e., whose names end in ${EXEEXT}.
EXE_FILES = ${INSTALLABLES} ${UTILITIES} ${DONT_INSTALL}

# =========================== Configuration ===========================

# MS-Windows resource files and resource compiler
EMACSRES = 
EMACS_MANIFEST = 
WINDRES = 

## Extra libraries to use when linking addpm.
LIBS_ADDPM = -lole32 -luuid

## Compilation and linking flags
BASE_CFLAGS = $(C_SWITCH_SYSTEM) $(C_SWITCH_MACHINE) \
	      $(WARN_CFLAGS) $(WERROR_CFLAGS) \
	      -I. -I${srcdir}

ALL_CFLAGS = ${BASE_CFLAGS} ${PROFILING_CFLAGS} ${LDFLAGS} ${CPPFLAGS} ${CFLAGS}
LINK_CFLAGS = ${BASE_CFLAGS} ${LDFLAGS} ${CFLAGS}
CPP_CFLAGS = ${BASE_CFLAGS} ${PROFILING_CFLAGS} ${CPPFLAGS} ${CFLAGS}

all: ${EXE_FILES}

.PHONY: all

## Install the internal utilities.  Until they are installed, we can
## just run them directly from nt/.
$(DESTDIR)${archlibdir}: all
	@echo
	@echo "Installing utilities run internally by Emacs."
	umask 022; ${MKDIR_P} "$(DESTDIR)${archlibdir}"
	exp_archlibdir=`cd "$(DESTDIR)${archlibdir}" && /bin/pwd`; \
	if [ "$$exp_archlibdir" != "`/bin/pwd`" ]; then \
	  for file in ${UTILITIES}; do \
	    $(INSTALL_PROGRAM) $(INSTALL_STRIP) $$file "$(DESTDIR)${archlibdir}/$$file" ; \
	  done ; \
        fi

.PHONY: install uninstall mostlyclean clean distclean maintainer-clean
.PHONY: extraclean check tags

install: $(DESTDIR)${archlibdir}
	@echo
	@echo "Installing utilities for users to run."
	umask 022; ${MKDIR_P} "$(DESTDIR)${bindir}"
	for file in ${INSTALLABLES} ; do \
	  $(INSTALL_PROGRAM) $(INSTALL_STRIP) $${file} "$(DESTDIR)${bindir}"/`echo $${file} | sed -e 's/${EXEEXT}$$//' -e '$(TRANSFORM)'`${EXEEXT} ; \
	done
	${MKDIR_P} "$(DESTDIR)${datadir}/emacs/$(version)"
	$(INSTALL_DATA) ${srcdir}/README.W32 "$(DESTDIR)${datadir}/emacs/$(version)"

uninstall:
	rm -f "$(DESTDIR)${datadir}/emacs/$(version)/README.W32"
	for file in ${INSTALLABLES}; do \
	  rm -f "$(DESTDIR)${bindir}"/`echo $${file} | sed -e 's/${EXEEXT}$$//' -e '$(TRANSFORM)'`${EXEEXT} ; \
	done
	if [ -d "$(DESTDIR)${archlibdir}" ]; then \
	  (cd "$(DESTDIR)${archlibdir}" && rm -f ${UTILITIES}) \
	fi

mostlyclean:
	-rm -f core *.o *.res

clean: mostlyclean
	-rm -f ${EXE_FILES}

distclean: clean
	-rm -f TAGS
	-rm -f Makefile

maintainer-clean: distclean
	true

extraclean: maintainer-clean
	-rm -f *~ \#*

## Test the contents of the directory.
check:
	@echo "We don't have any tests for the nt/ directory yet."

tags: TAGS
TAGS: ${EXE_FILES:${EXEEXT}=.c}
	../lib-src/etags *.[ch]

## Build the programs
addsection${EXEEXT}: ${srcdir}/addsection.c
	$(CC) ${ALL_CFLAGS} ${srcdir}/addsection.c -o addsection${EXEEXT}

addpm${EXEEXT}: ${srcdir}/addpm.c ../src/epaths.h
	$(CC) ${ALL_CFLAGS} ${srcdir}/addpm.c $(LIBS_ADDPM) -o addpm${EXEEXT}

ddeclient${EXEEXT}: ${srcdir}/ddeclient.c
	$(CC) ${ALL_CFLAGS} ${srcdir}/ddeclient.c -o ddeclient${EXEEXT}

cmdproxy${EXEEXT}: ${srcdir}/cmdproxy.c
	$(CC) ${ALL_CFLAGS} ${srcdir}/cmdproxy.c -o cmdproxy${EXEEXT}

runemacs${EXEEXT}: ${srcdir}/runemacs.c $(EMACSRES)
	$(CC) ${ALL_CFLAGS} ${srcdir}/runemacs.c $(EMACSRES) -mwindows \
         -o runemacs${EXEEXT}

emacs.res: ${srcdir}/emacs.rc ${srcdir}/icons/emacs.ico ${srcdir}/$(EMACS_MANIFEST)
	${WINDRES} -I ${srcdir} -O coff -o emacs.res ${srcdir}/emacs.rc
