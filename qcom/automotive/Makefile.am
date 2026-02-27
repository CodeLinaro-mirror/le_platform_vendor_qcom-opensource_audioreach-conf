# No recursion at all
SUBDIRS =

# -------- ALSA (common) --------
alsaconfddir = $(sysconfdir)/alsa/conf.d
alsaconfd_DATA = alsalib/agm.conf

alsaucmvirtdir = $(datadir)/alsa/ucm2/conf.virt.d
alsaucmvirt_DATA = alsalib/agmvirtualsndcard.conf

# -------- SA8797 specific --------
if SA8797

# ALSA UCM usecase
alsaucmvirt_DATA += \
    alsalib/sa8797/A2BPlayback.conf \
    alsalib/sa8797/A2BRecord.conf \
    alsalib/sa8797/ADCRecord.conf \
    alsalib/sa8797/DACPlayback.conf

# tinyalsa card definition
carddefdir = $(sysconfdir)
carddef_DATA = tinyalsa/sa8797/card-defs.xml

# pkg-config metadata
pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = tinyalsa/sa8797/config.pc

# ship template
EXTRA_DIST = tinyalsa/sa8797/config.pc.in

endif
