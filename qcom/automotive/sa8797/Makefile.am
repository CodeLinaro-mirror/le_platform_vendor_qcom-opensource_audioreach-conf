pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = config.pc
EXTRA_DIST = $(pkgconfig_DATA)

AM_CFLAGS = -Wall -Werror

config_carddef = card-defs.xml
config_carddefdir = $(sysconfdir)
config_includedir = $(includedir)
config_include_DATA = $(config_carddef)

# install xml files under /etc
root_etcdir      = "/etc"
root_etc_SCRIPTS = card-defs.xml
install-data-hook:
	chmod  go-x $(DESTDIR)$(root_etcdir)/card-defs.xml