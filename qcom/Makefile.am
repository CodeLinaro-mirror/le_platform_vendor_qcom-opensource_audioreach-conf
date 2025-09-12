pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = kvh2xml.pc
EXTRA_DIST = $(pkgconfig_DATA)

acdbdata_headers = kvh2xml.h
acdbdata_includedir = $(includedir)/acdbdata
acdbdata_include_HEADERS = $(acdbdata_headers)

if AUTOMOTIVE
SUBDIRS = automotive
endif

#if QLI
#SUBDIRS = qli
#endif