plugin_LTLIBRARIES = motion.la
motion_la_LDFLAGS = -avoid-version -module -shared
motion_la_LIBADD = libaffine.la
motion_la_SOURCES = motion.C motionwindow.C
noinst_LTLIBRARIES = libaffine.la
libaffine_la_LDFLAGS = 
libaffine_la_LIBADD = 
libaffine_la_SOURCES = affine.C
AM_CXXFLAGS = $(LARGEFILE_CFLAGS)

AM_CPPFLAGS = -I$(top_srcdir)/guicast -I$(top_srcdir)/cinelerra -I$(top_srcdir)/quicktime
LIBTOOL = $(SHELL) $(top_builddir)/libtool $(LTCXX_FLAGS)

noinst_HEADERS = \
	affine.h affine.inc \
	motion.h motion.inc \
	motionwindow.h motionwindow.inc
EXTRA_DIST = picon.png

BUILT_SOURCES = picon_png.h
picon_png.h: picon.png
	$(top_builddir)/guicast/pngtoh $^ || { rm -f $@; exit 1; }
clean-local:
	$(RM) picon_png.h
