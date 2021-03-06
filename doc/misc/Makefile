### doc/misc/Makefile.  Generated from Makefile.in by configure.

# Copyright (C) 1994, 1996-2014 Free Software Foundation, Inc.

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

SHELL = /bin/sh

# Where to find the source code.  $(srcdir) will be the man-aux
# subdirectory of the source tree.  This is
# set by the configure script's `--srcdir' option.
srcdir=.

version=24.3.92

## Where the output files go.
buildinfodir = $(srcdir)/../../info
## Directory with emacsver.texi.
emacsdir = $(srcdir)/../emacs

prefix = /usr/local
datarootdir = ${prefix}/share
datadir = ${datarootdir}
PACKAGE_TARNAME = emacs
docdir = ${datarootdir}/doc/${PACKAGE_TARNAME}
dvidir = ${docdir}
htmldir = ${docdir}
pdfdir = ${docdir}
psdir = ${docdir}

MKDIR_P = ../../build-aux/install-sh -c -d

GZIP_PROG = /usr/bin/gzip

HTML_OPTS = --no-split --html

INFO_EXT=.info
# Options used only when making info output.
INFO_OPTS=--no-split

INSTALL = /usr/bin/install -c
INSTALL_DATA = ${INSTALL} -m 644

# The makeinfo program is part of the Texinfo distribution.
# Use --force so that it generates output even if there are errors.
MAKEINFO = /usr/bin/makeinfo
MAKEINFO_OPTS = --force -I$(emacsdir)

## On MS Windows, efaq-w32; otherwise blank.
DOCMISC_W32 = 

## Info files to build and install on all platforms.
INFO_COMMON = ada-mode auth autotype bovine calc ccmode cl \
	dbus dired-x ebrowse ede ediff edt eieio \
	emacs-mime epa erc ert eshell eudc efaq eww \
	flymake forms gnus emacs-gnutls htmlfontify idlwave ido info.info \
	mairix-el message mh-e newsticker nxml-mode octave-mode \
	org pcl-cvs pgg rcirc remember reftex sasl \
	sc semantic ses sieve smtpmail speedbar srecode todo-mode tramp \
	url vip viper widget wisent woman

## Info files to install on current platform.
INFO_INSTALL = $(INFO_COMMON) $(DOCMISC_W32)

## Info files to build on current platform.
## This is all of them, even though they might not all get installed,
## because the info files are pre-built in release tarfiles.
INFO_TARGETS = $(INFO_COMMON) efaq-w32

# There are some naming differences between the info targets and the other
# targets, so let's resolve them here.
TARGETS_1 = $(INFO_INSTALL:ccmode=cc-mode)
TARGETS = $(TARGETS_1:info.info=info)

DVI_TARGETS  = $(TARGETS:=.dvi)
HTML_TARGETS = $(TARGETS:=.html)
PDF_TARGETS  = $(TARGETS:=.pdf)
PS_TARGETS   = $(TARGETS:=.ps)

TEXI2DVI = texi2dvi
TEXI2PDF = texi2pdf
DVIPS = dvips

ENVADD = TEXINPUTS="$(srcdir):$(emacsdir):$(TEXINPUTS)" \
         MAKEINFO="$(MAKEINFO) $(MAKEINFO_OPTS)"

mkinfodir = @${MKDIR_P} ${buildinfodir}

gfdl = ${srcdir}/doclicense.texi

.PHONY: info dvi html pdf ps echo-info
## Prevent implicit rule triggering for foo.info.
.SUFFIXES:

.SUFFIXES: .ps .dvi

.dvi.ps:
	$(DVIPS) -o $@ $<

# Default.
info: $(INFO_TARGETS)

## Used by top-level Makefile.
## Base file names of output info files.
echo-info:
	@echo "$(INFO_INSTALL) " | \
	  sed -e 's|[^ ]*/||g' -e 's/\.info//g' -e "s/  */$(INFO_EXT) /g"

dvi: $(DVI_TARGETS)

html: $(HTML_TARGETS)

pdf: $(PDF_TARGETS)

ps: $(PS_TARGETS)

# Note that all the Info targets build the Info files in srcdir.
# There is no provision for Info files to exist in the build directory.
# In a distribution of Emacs, the Info files should be up to date.

# Note: "<" is not portable in ordinary make rules.

ada_mode_deps = ${srcdir}/ada-mode.texi ${gfdl}
ada-mode : $(buildinfodir)/ada-mode$(INFO_EXT)
$(buildinfodir)/ada-mode$(INFO_EXT): $(ada_mode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ada-mode.texi
ada-mode.dvi: $(ada_mode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ada-mode.texi
ada-mode.pdf: $(ada_mode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ada-mode.texi
ada-mode.html: $(ada_mode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ada-mode.texi

auth_deps = ${srcdir}/auth.texi ${gfdl}
auth : $(buildinfodir)/auth$(INFO_EXT)
$(buildinfodir)/auth$(INFO_EXT): $(auth_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/auth.texi
auth.dvi: $(auth_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/auth.texi
auth.pdf: $(auth_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/auth.texi
auth.html: $(auth_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/auth.texi

autotype_deps = ${srcdir}/autotype.texi ${gfdl}
autotype : $(buildinfodir)/autotype$(INFO_EXT)
$(buildinfodir)/autotype$(INFO_EXT): $(autotype_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/autotype.texi
autotype.dvi: $(autotype_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/autotype.texi
autotype.pdf: $(autotype_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/autotype.texi
autotype.html: $(autotype_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/autotype.texi

bovine_deps = ${srcdir}/bovine.texi ${gfdl}
bovine : $(buildinfodir)/bovine$(INFO_EXT)
$(buildinfodir)/bovine$(INFO_EXT): $(bovine_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/bovine.texi
bovine.dvi: $(bovine_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/bovine.texi
bovine.pdf: $(bovine_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/bovine.texi
bovine.html: $(bovine_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/bovine.texi

calc_deps = ${srcdir}/calc.texi $(emacsdir)/emacsver.texi ${gfdl}
calc : $(buildinfodir)/calc$(INFO_EXT)
$(buildinfodir)/calc$(INFO_EXT): $(calc_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/calc.texi
calc.dvi: $(calc_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/calc.texi
calc.pdf: $(calc_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/calc.texi
calc.html: $(calc_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/calc.texi

cc_mode_deps = ${srcdir}/cc-mode.texi ${gfdl}
ccmode : $(buildinfodir)/ccmode$(INFO_EXT)
$(buildinfodir)/ccmode$(INFO_EXT): $(cc_mode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/cc-mode.texi
cc-mode.dvi: $(cc_mode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/cc-mode.texi
cc-mode.pdf: $(cc_mode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/cc-mode.texi
cc-mode.html: $(cc_mode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/cc-mode.texi

cl_deps = ${srcdir}/cl.texi $(emacsdir)/emacsver.texi ${gfdl}
cl : $(buildinfodir)/cl$(INFO_EXT)
$(buildinfodir)/cl$(INFO_EXT): $(cl_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/cl.texi
cl.dvi: $(cl_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/cl.texi
cl.pdf: $(cl_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/cl.texi
cl.html: $(cl_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/cl.texi

dbus_deps = ${srcdir}/dbus.texi ${gfdl}
dbus : $(buildinfodir)/dbus$(INFO_EXT)
$(buildinfodir)/dbus$(INFO_EXT): $(dbus_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/dbus.texi
dbus.dvi: $(dbus_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/dbus.texi
dbus.pdf: $(dbus_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/dbus.texi
dbus.html: $(dbus_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/dbus.texi

dired_x_deps = ${srcdir}/dired-x.texi $(emacsdir)/emacsver.texi ${gfdl}
dired-x : $(buildinfodir)/dired-x$(INFO_EXT)
$(buildinfodir)/dired-x$(INFO_EXT): $(dired_x_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/dired-x.texi
dired-x.dvi: $(dired_x_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/dired-x.texi
dired-x.pdf: $(dired_x_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/dired-x.texi
dired-x.html: $(dired_x_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/dired-x.texi

ebrowse_deps = ${srcdir}/ebrowse.texi ${gfdl}
ebrowse : $(buildinfodir)/ebrowse$(INFO_EXT)
$(buildinfodir)/ebrowse$(INFO_EXT): $(ebrowse_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ebrowse.texi
ebrowse.dvi: $(ebrowse_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ebrowse.texi
ebrowse.pdf: $(ebrowse_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ebrowse.texi
ebrowse.html: $(ebrowse_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ebrowse.texi

ede_deps = ${srcdir}/ede.texi ${gfdl}
ede : $(buildinfodir)/ede$(INFO_EXT)
$(buildinfodir)/ede$(INFO_EXT): $(ede_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ede.texi
ede.dvi: $(ede_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ede.texi
ede.pdf: $(ede_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ede.texi
ede.html: $(ede_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ede.texi

ediff_deps = ${srcdir}/ediff.texi ${gfdl}
ediff : $(buildinfodir)/ediff$(INFO_EXT)
$(buildinfodir)/ediff$(INFO_EXT): $(ediff_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ediff.texi
ediff.dvi: $(ediff_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ediff.texi
ediff.pdf: $(ediff_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ediff.texi
ediff.html: $(ediff_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ediff.texi

edt_deps = ${srcdir}/edt.texi ${gfdl}
edt : $(buildinfodir)/edt$(INFO_EXT)
$(buildinfodir)/edt$(INFO_EXT): $(edt_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/edt.texi
edt.dvi: $(edt_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/edt.texi
edt.pdf: $(edt_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/edt.texi
edt.html: $(edt_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/edt.texi

## No gfdl dependency.
efaq_deps = ${srcdir}/efaq.texi $(emacsdir)/emacsver.texi
efaq : $(buildinfodir)/efaq$(INFO_EXT)
$(buildinfodir)/efaq$(INFO_EXT): $(efaq_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/efaq.texi
efaq.dvi: $(efaq_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/efaq.texi
efaq.pdf: $(efaq_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/efaq.texi
efaq.html: $(efaq_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/efaq.texi

efaq_w32_deps = ${srcdir}/efaq-w32.texi $(emacsdir)/emacsver.texi
efaq-w32 : $(buildinfodir)/efaq-w32$(INFO_EXT)
$(buildinfodir)/efaq-w32$(INFO_EXT): $(efaq_w32_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/efaq-w32.texi
efaq-w32.dvi: $(efaq_w32_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/efaq-w32.texi
efaq-w32.pdf: $(efaq_w32_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/efaq-w32.texi
efaq-w32.html: $(efaq_w32_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/efaq-w32.texi

eieio_deps = ${srcdir}/eieio.texi ${gfdl}
eieio : $(buildinfodir)/eieio$(INFO_EXT)
$(buildinfodir)/eieio$(INFO_EXT): $(eieio_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/eieio.texi
eieio.dvi: $(eieio_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/eieio.texi
eieio.pdf: $(eieio_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/eieio.texi
eieio.html: $(eieio_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/eieio.texi

emacs_gnutls_deps = ${srcdir}/emacs-gnutls.texi ${gfdl}
emacs-gnutls : $(buildinfodir)/emacs-gnutls$(INFO_EXT)
$(buildinfodir)/emacs-gnutls$(INFO_EXT): $(emacs_gnutls_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/emacs-gnutls.texi
emacs-gnutls.dvi: $(emacs_gnutls_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/emacs-gnutls.texi
emacs-gnutls.pdf: $(emacs_gnutls_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/emacs-gnutls.texi
emacs-gnutls.html: $(emacs_gnutls_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/emacs-gnutls.texi

emacs_mime_deps = ${srcdir}/emacs-mime.texi ${gfdl}
emacs-mime : $(buildinfodir)/emacs-mime$(INFO_EXT)
$(buildinfodir)/emacs-mime$(INFO_EXT): $(emacs_mime_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) --enable-encoding -o $@ ${srcdir}/emacs-mime.texi
emacs-mime.dvi: $(emacs_mime_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/emacs-mime.texi
emacs-mime.pdf: $(emacs_mime_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/emacs-mime.texi
emacs-mime.html: $(emacs_mime_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) --enable-encoding -o $@ ${srcdir}/emacs-mime.texi

epa_deps = ${srcdir}/epa.texi ${gfdl}
epa : $(buildinfodir)/epa$(INFO_EXT)
$(buildinfodir)/epa$(INFO_EXT): $(epa_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/epa.texi
epa.dvi: $(epa_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/epa.texi
epa.pdf: $(epa_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/epa.texi
epa.html: $(epa_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/epa.texi

erc_deps = ${srcdir}/erc.texi $(emacsdir)/emacsver.texi ${gfdl}
erc : $(buildinfodir)/erc$(INFO_EXT)
$(buildinfodir)/erc$(INFO_EXT): $(erc_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/erc.texi
erc.dvi: $(erc_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/erc.texi
erc.pdf: $(erc_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/erc.texi
erc.html: $(erc_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/erc.texi

ert_deps = ${srcdir}/ert.texi ${gfdl}
ert : $(buildinfodir)/ert$(INFO_EXT)
$(buildinfodir)/ert$(INFO_EXT): $(ert_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ert.texi
ert.dvi: $(ert_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ert.texi
ert.pdf: $(ert_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ert.texi
ert.html: $(ert_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ert.texi

eshell_deps = ${srcdir}/eshell.texi ${gfdl}
eshell : $(buildinfodir)/eshell$(INFO_EXT)
$(buildinfodir)/eshell$(INFO_EXT): $(eshell_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/eshell.texi
eshell.dvi: $(eshell_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/eshell.texi
eshell.pdf: $(eshell_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/eshell.texi
eshell.html: $(eshell_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/eshell.texi

eudc_deps = ${srcdir}/eudc.texi ${gfdl}
eudc : $(buildinfodir)/eudc$(INFO_EXT)
$(buildinfodir)/eudc$(INFO_EXT): $(eudc_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/eudc.texi
eudc.dvi: $(eudc_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/eudc.texi
eudc.pdf: $(eudc_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/eudc.texi
eudc.html: $(eudc_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/eudc.texi

eww_deps = ${srcdir}/eww.texi ${gfdl}
eww : $(buildinfodir)/eww$(INFO_EXT)
$(buildinfodir)/eww$(INFO_EXT): $(eww_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/eww.texi
eww.dvi: $(eww_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/eww.texi
eww.pdf: $(eww_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/eww.texi
eww.html: $(eww_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/eww.texi

flymake_deps = ${srcdir}/flymake.texi ${gfdl}
flymake : $(buildinfodir)/flymake$(INFO_EXT)
$(buildinfodir)/flymake$(INFO_EXT): $(flymake_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/flymake.texi
flymake.dvi: $(flymake_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/flymake.texi
flymake.pdf: $(flymake_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/flymake.texi
flymake.html: $(flymake_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/flymake.texi

forms_deps = ${srcdir}/forms.texi ${gfdl}
forms : $(buildinfodir)/forms$(INFO_EXT)
$(buildinfodir)/forms$(INFO_EXT): $(forms_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/forms.texi
forms.dvi: $(forms_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/forms.texi
forms.pdf: $(forms_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/forms.texi
forms.html: $(forms_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/forms.texi

## gnus/message/emacs-mime/sieve/pgg are part of Gnus.
gnus_deps = ${srcdir}/gnus.texi ${srcdir}/gnus-faq.texi ${gfdl}
gnus : $(buildinfodir)/gnus$(INFO_EXT)
$(buildinfodir)/gnus$(INFO_EXT): $(gnus_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/gnus.texi
gnus.dvi: $(gnus_deps)
	sed -e '/@iflatex/,/@end iflatex/d' ${srcdir}/gnus.texi > gnustmp.texi
	$(ENVADD) $(TEXI2DVI) gnustmp.texi
	cp gnustmp.dvi $@
	rm gnustmp.*
gnus.pdf: $(gnus_deps)
	sed -e '/@iflatex/,/@end iflatex/d' ${srcdir}/gnus.texi > gnustmp.texi
	$(ENVADD) $(TEXI2PDF) gnustmp.texi
	cp gnustmp.pdf $@
	rm gnustmp.*
gnus.html: $(gnus_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/gnus.texi

htmlfontify_deps = ${srcdir}/htmlfontify.texi ${gfdl}
htmlfontify : $(buildinfodir)/htmlfontify$(INFO_EXT)
$(buildinfodir)/htmlfontify$(INFO_EXT): $(htmlfontify_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/htmlfontify.texi
htmlfontify.dvi: $(htmlfontify_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/htmlfontify.texi
htmlfontify.pdf: $(htmlfontify_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/htmlfontify.texi
htmlfontify.html: $(htmlfontify_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/htmlfontify.texi

idlwave_deps = ${srcdir}/idlwave.texi ${gfdl}
idlwave : $(buildinfodir)/idlwave$(INFO_EXT)
# NB this one needs --no-split even without a .info extension.
$(buildinfodir)/idlwave$(INFO_EXT): $(idlwave_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/idlwave.texi
idlwave.dvi: $(idlwave_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/idlwave.texi
idlwave.pdf: $(idlwave_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/idlwave.texi
idlwave.html: $(idlwave_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/idlwave.texi

ido_deps = ${srcdir}/ido.texi $(emacsdir)/emacsver.texi ${gfdl}
ido : $(buildinfodir)/ido$(INFO_EXT)
$(buildinfodir)/ido$(INFO_EXT): $(ido_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ido.texi
ido.dvi: $(ido_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ido.texi
ido.pdf: $(ido_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ido.texi
ido.html: $(ido_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ido.texi

info_deps = ${srcdir}/info.texi ${gfdl}
# Avoid name clash with overall "info" target.
info.info : $(buildinfodir)/info$(INFO_EXT)
# NB this one needs --no-split even without a .info extension.
$(buildinfodir)/info$(INFO_EXT): $(info_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/info.texi
info.dvi: $(info_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/info.texi
info.pdf: $(info_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/info.texi
info.html: $(info_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/info.texi

mairix_el_deps = ${srcdir}/mairix-el.texi ${gfdl}
mairix-el : $(buildinfodir)/mairix-el$(INFO_EXT)
$(buildinfodir)/mairix-el$(INFO_EXT): $(mairix_el_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/mairix-el.texi
mairix-el.dvi: $(mairix_el_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/mairix-el.texi
mairix-el.pdf: $(mairix_el_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/mairix-el.texi
mairix-el.html: $(mairix_el_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/mairix-el.texi

message_deps = ${srcdir}/message.texi ${gfdl}
message : $(buildinfodir)/message$(INFO_EXT)
$(buildinfodir)/message$(INFO_EXT): $(message_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/message.texi
message.dvi: $(message_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/message.texi
message.pdf: $(message_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/message.texi
message.html: $(message_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/message.texi

mh_e_deps = ${srcdir}/mh-e.texi ${gfdl}
mh-e : $(buildinfodir)/mh-e$(INFO_EXT)
$(buildinfodir)/mh-e$(INFO_EXT): $(mh_e_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/mh-e.texi
mh-e.dvi: $(mh_e_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/mh-e.texi
mh-e.pdf: $(mh_e_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/mh-e.texi
mh-e.html: $(mh_e_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/mh-e.texi

newsticker_deps = ${srcdir}/newsticker.texi ${gfdl}
newsticker : $(buildinfodir)/newsticker$(INFO_EXT)
$(buildinfodir)/newsticker$(INFO_EXT): $(newsticker_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/newsticker.texi
newsticker.dvi: $(newsticker_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/newsticker.texi
newsticker.pdf: $(newsticker_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/newsticker.texi
newsticker.html: $(newsticker_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/newsticker.texi

nxml_mode_deps = ${srcdir}/nxml-mode.texi ${gfdl}
nxml-mode : $(buildinfodir)/nxml-mode$(INFO_EXT)
$(buildinfodir)/nxml-mode$(INFO_EXT): $(nxml_mode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/nxml-mode.texi
nxml-mode.dvi: $(nxml_mode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/nxml-mode.texi
nxml-mode.pdf: $(nxml_mode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/nxml-mode.texi
nxml-mode.html: $(nxml_mode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/nxml-mode.texi

octave_mode_deps = ${srcdir}/octave-mode.texi ${gfdl}
octave-mode : $(buildinfodir)/octave-mode$(INFO_EXT)
$(buildinfodir)/octave-mode$(INFO_EXT): $(octave_mode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/octave-mode.texi
octave-mode.dvi: $(octave_mode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/octave-mode.texi
octave-mode.pdf: $(octave_mode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/octave-mode.texi
octave-mode.html: $(octave_mode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/octave-mode.texi

org_deps = ${srcdir}/org.texi ${gfdl}
org : $(buildinfodir)/org$(INFO_EXT)
$(buildinfodir)/org$(INFO_EXT): $(org_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/org.texi
org.dvi: $(org_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/org.texi
org.pdf: $(org_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/org.texi
org.html: $(org_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/org.texi

pcl_cvs_deps = ${srcdir}/pcl-cvs.texi ${gfdl}
pcl-cvs : $(buildinfodir)/pcl-cvs$(INFO_EXT)
$(buildinfodir)/pcl-cvs$(INFO_EXT): $(pcl_cvs_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/pcl-cvs.texi
pcl-cvs.dvi: $(pcl_cvs_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/pcl-cvs.texi
pcl-cvs.pdf: $(pcl_cvs_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/pcl-cvs.texi
pcl-cvs.html: $(pcl_cvs_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/pcl-cvs.texi

pgg_deps = ${srcdir}/pgg.texi ${gfdl}
pgg : $(buildinfodir)/pgg$(INFO_EXT)
$(buildinfodir)/pgg$(INFO_EXT): $(pgg_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/pgg.texi
pgg.dvi: $(pgg_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/pgg.texi
pgg.pdf: $(pgg_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/pgg.texi
pgg.html: $(pgg_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/pgg.texi

rcirc_deps = ${srcdir}/rcirc.texi ${gfdl}
rcirc : $(buildinfodir)/rcirc$(INFO_EXT)
$(buildinfodir)/rcirc$(INFO_EXT): $(rcirc_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/rcirc.texi
rcirc.dvi: $(rcirc_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/rcirc.texi
rcirc.pdf: $(rcirc_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/rcirc.texi
rcirc.html: $(rcirc_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/rcirc.texi

reftex_deps = ${srcdir}/reftex.texi $(emacsdir)/emacsver.texi ${gfdl}
reftex : $(buildinfodir)/reftex$(INFO_EXT)
$(buildinfodir)/reftex$(INFO_EXT): $(reftex_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/reftex.texi
reftex.dvi: $(reftex_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/reftex.texi
reftex.pdf: $(reftex_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/reftex.texi
reftex.html: $(reftex_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/reftex.texi

remember_deps = ${srcdir}/remember.texi ${gfdl}
remember : $(buildinfodir)/remember$(INFO_EXT)
$(buildinfodir)/remember$(INFO_EXT): $(remember_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/remember.texi
remember.dvi: $(remember_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/remember.texi
remember.pdf: $(remember_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/remember.texi
remember.html: $(remember_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/remember.texi

sasl_deps = ${srcdir}/sasl.texi ${gfdl}
sasl : $(buildinfodir)/sasl$(INFO_EXT)
$(buildinfodir)/sasl$(INFO_EXT): $(sasl_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/sasl.texi
sasl.dvi: $(sasl_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/sasl.texi
sasl.pdf: $(sasl_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/sasl.texi
sasl.html: $(sasl_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/sasl.texi

sc_deps = ${srcdir}/sc.texi ${gfdl}
sc : $(buildinfodir)/sc$(INFO_EXT)
$(buildinfodir)/sc$(INFO_EXT): $(sc_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/sc.texi
sc.dvi: $(sc_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/sc.texi
sc.pdf: $(sc_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/sc.texi
sc.html: $(sc_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/sc.texi

semantic_deps = ${srcdir}/semantic.texi ${srcdir}/sem-user.texi ${gfdl}
semantic : $(buildinfodir)/semantic$(INFO_EXT)
$(buildinfodir)/semantic$(INFO_EXT): $(semantic_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/semantic.texi
semantic.dvi: $(semantic_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/semantic.texi
semantic.pdf: $(semantic_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/semantic.texi
semantic.html: $(semantic_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/semantic.texi

ses_deps = ${srcdir}/ses.texi ${gfdl}
ses : $(buildinfodir)/ses$(INFO_EXT)
$(buildinfodir)/ses$(INFO_EXT): $(ses_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/ses.texi
ses.dvi: $(ses_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/ses.texi
ses.pdf: $(ses_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/ses.texi
ses.html: $(ses_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/ses.texi

sieve_deps = ${srcdir}/sieve.texi ${gfdl}
sieve : $(buildinfodir)/sieve$(INFO_EXT)
$(buildinfodir)/sieve$(INFO_EXT): $(sieve_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/sieve.texi
sieve.dvi: $(sieve_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/sieve.texi
sieve.pdf: $(sieve_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/sieve.texi
sieve.html: $(sieve_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/sieve.texi

smtpmail_deps = ${srcdir}/smtpmail.texi ${gfdl}
smtpmail : $(buildinfodir)/smtpmail$(INFO_EXT)
$(buildinfodir)/smtpmail$(INFO_EXT): $(smtpmail_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/smtpmail.texi
smtpmail.dvi: $(smtpmail_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/smtpmail.texi
smtpmail.pdf: $(smtpmail_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/smtpmail.texi
smtpmail.html: $(smtpmail_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/smtpmail.texi

speedbar_deps = ${srcdir}/speedbar.texi ${gfdl}
speedbar : $(buildinfodir)/speedbar$(INFO_EXT)
$(buildinfodir)/speedbar$(INFO_EXT): $(speedbar_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/speedbar.texi
speedbar.dvi: $(speedbar_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/speedbar.texi
speedbar.pdf: $(speedbar_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/speedbar.texi
speedbar.html: $(speedbar_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/speedbar.texi

srecode_deps = ${srcdir}/srecode.texi ${gfdl}
srecode : $(buildinfodir)/srecode$(INFO_EXT)
$(buildinfodir)/srecode$(INFO_EXT): $(srecode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/srecode.texi
srecode.dvi: $(srecode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/srecode.texi
srecode.pdf: $(srecode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/srecode.texi
srecode.html: $(srecode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/srecode.texi

todo_mode_deps = ${srcdir}/todo-mode.texi ${gfdl}
todo-mode : $(buildinfodir)/todo-mode$(INFO_EXT)
$(buildinfodir)/todo-mode$(INFO_EXT): $(todo_mode_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/todo-mode.texi
todo-mode.dvi: $(todo_mode_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/todo-mode.texi
todo-mode.pdf: $(todo_mode_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/todo-mode.texi
todo-mode.html: $(todo_mode_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/todo-mode.texi

tramp_deps = ${srcdir}/tramp.texi ${srcdir}/trampver.texi ${gfdl}
tramp : $(buildinfodir)/tramp$(INFO_EXT)
$(buildinfodir)/tramp$(INFO_EXT): $(tramp_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ -D emacs ${srcdir}/tramp.texi
tramp.dvi: $(tramp_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/tramp.texi
tramp.pdf: $(tramp_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/tramp.texi
tramp.html: $(tramp_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ -D emacs ${srcdir}/tramp.texi

url_deps = ${srcdir}/url.texi ${gfdl}
url : $(buildinfodir)/url$(INFO_EXT)
$(buildinfodir)/url$(INFO_EXT): $(url_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/url.texi
url.dvi: $(url_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/url.texi
url.pdf: $(url_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/url.texi
url.html: $(url_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/url.texi

vip_deps = ${srcdir}/vip.texi ${gfdl}
vip : $(buildinfodir)/vip$(INFO_EXT)
$(buildinfodir)/vip$(INFO_EXT): $(vip_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/vip.texi
vip.dvi: $(vip_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/vip.texi
vip.pdf: $(vip_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/vip.texi
vip.html: $(vip_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/vip.texi

viper_deps = ${srcdir}/viper.texi ${gfdl}
viper : $(buildinfodir)/viper$(INFO_EXT)
$(buildinfodir)/viper$(INFO_EXT): $(viper_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/viper.texi
viper.dvi: $(viper_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/viper.texi
viper.pdf: $(viper_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/viper.texi
viper.html: $(viper_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/viper.texi

widget_deps = ${srcdir}/wisent.texi ${gfdl}
widget : $(buildinfodir)/widget$(INFO_EXT)
$(buildinfodir)/widget$(INFO_EXT): $(widget_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/widget.texi
widget.dvi: $(widget_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/widget.texi
widget.pdf: $(widget_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/widget.texi
widget.html: $(widget_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/widget.texi

wisent_deps = ${srcdir}/wisent.texi ${gfdl}
wisent : $(buildinfodir)/wisent$(INFO_EXT)
$(buildinfodir)/wisent$(INFO_EXT): $(wisent_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/wisent.texi
wisent.dvi: $(wisent_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/wisent.texi
wisent.pdf: $(wisent_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/wisent.texi
wisent.html: $(wisent_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/wisent.texi

woman_deps = ${srcdir}/woman.texi $(emacsdir)/emacsver.texi ${gfdl}
woman : $(buildinfodir)/woman$(INFO_EXT)
$(buildinfodir)/woman$(INFO_EXT): $(woman_deps)
	$(mkinfodir)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(INFO_OPTS) -o $@ ${srcdir}/woman.texi
woman.dvi: $(woman_deps)
	$(ENVADD) $(TEXI2DVI) ${srcdir}/woman.texi
woman.pdf: $(woman_deps)
	$(ENVADD) $(TEXI2PDF) ${srcdir}/woman.texi
woman.html: $(woman_deps)
	$(MAKEINFO) $(MAKEINFO_OPTS) $(HTML_OPTS) -o $@ ${srcdir}/woman.texi

.PHONY: mostlyclean clean distclean maintainer-clean

mostlyclean:
	rm -f *.aux *.log *.toc *.c[mp] *.c[mp]s *.fn *.fns \
	  *.ky *.kys *.op *.ops *.p[gj] *.p[gj]s *.sc *.scs *.ss \
	  *.t[gp] *.t[gp]s *.vr *.vrs
	rm -f gnustmp.*

clean: mostlyclean
	rm -f $(DVI_TARGETS) $(HTML_TARGETS) $(PDF_TARGETS) $(PS_TARGETS)
	rm -f efaq-w32.dvi efaq-w32.html efaq-w32.pdf efaq-w32.ps
	rm -f emacs-misc-${version}.tar*

distclean: clean
	rm -f Makefile

## buildinfodir is relative to srcdir.
infoclean:
	cd $(buildinfodir); for file in $(INFO_TARGETS); do \
	  file=`echo $${file} | sed 's/\.info$$//'`${INFO_EXT}; \
	  rm -f $${file} $${file}-[1-9] $${file}-[1-9][0-9]; \
	done

maintainer-clean: distclean infoclean

dist:
	rm -rf emacs-misc-${version}
	mkdir emacs-misc-${version}
	cp ${srcdir}/*.texi ${srcdir}/texinfo.tex \
	  $(emacsdir)/emacsver.texi ${srcdir}/ChangeLog* \
	  emacs-misc-${version}/
	sed -e 's/@sr[c]dir@/./' \
	  -e 's/^\(emacsdir *=\).*/\1 ./' \
	  -e 's/^\(buildinfodir *=\).*/\1 ./' \
	  -e 's/^\(clean:.*\)/\1 infoclean/' \
	  -e "s/@ver[s]ion@/${version}/" \
	  -e 's/@MAKE[I]NFO@/makeinfo/' -e 's/@MK[D]IR_P@/mkdir -p/' \
	  -e 's/@IN[F]O_EXT@/.info/' -e 's/@IN[F]O_OPTS@//' \
	  ${srcdir}/Makefile.in > emacs-misc-${version}/Makefile
	@if grep '@[a-zA-Z_]*@' emacs-misc-${version}/Makefile; then \
	  echo "Unexpanded configure variables in Makefile?" 1>&2; exit 1; \
	fi
	tar -cf emacs-misc-${version}.tar emacs-misc-${version}
	rm -rf emacs-misc-${version}


.PHONY: install-dvi install-html install-pdf install-ps install-doc

install-dvi: dvi
	umask 022; $(MKDIR_P) "$(DESTDIR)$(dvidir)"
	$(INSTALL_DATA) $(DVI_TARGETS) "$(DESTDIR)$(dvidir)"
install-html: html
	umask 022; $(MKDIR_P) "$(DESTDIR)$(htmldir)"
	$(INSTALL_DATA) $(HTML_TARGETS) "$(DESTDIR)$(htmldir)"
install-pdf: pdf
	 umask 022;$(MKDIR_P) "$(DESTDIR)$(pdfdir)"
	$(INSTALL_DATA) $(PDF_TARGETS) "$(DESTDIR)$(pdfdir)"
install-ps: ps
	umask 022; $(MKDIR_P) "$(DESTDIR)$(psdir)"
	for file in $(PS_TARGETS); do \
	  $(INSTALL_DATA) $${file} "$(DESTDIR)$(psdir)"; \
	  [ -n "${GZIP_PROG}" ] || continue; \
	  rm -f "$(DESTDIR)$(psdir)/$${file}.gz"; \
	  ${GZIP_PROG} -9n "$(DESTDIR)$(psdir)/$${file}"; \
	done

## Top-level Makefile installs the info pages.
install-doc: install-dvi install-html install-pdf install-ps



.PHONY: uninstall-dvi uninstall-html uninstall-pdf uninstall-ps uninstall-doc

uninstall-dvi:
	for file in $(DVI_TARGETS); do \
	  rm -f "$(DESTDIR)$(dvidir)/$${file}"; \
	done
uninstall-html:
	for file in $(HTML_TARGETS); do \
	  rm -f "$(DESTDIR)$(htmldir)/$${file}"; \
	done
uninstall-ps:
	ext= ; [ -n "${GZIP_PROG}" ] && ext=.gz; \
	for file in $(PS_TARGETS); do \
	  rm -f "$(DESTDIR)$(psdir)/$${file}$${ext}"; \
	done
uninstall-pdf:
	for file in $(PDF_TARGETS); do \
	  rm -f "$(DESTDIR)$(pdfdir)/$${file}"; \
	done

uninstall-doc: uninstall-dvi uninstall-html uninstall-pdf uninstall-ps


### Makefile ends here
