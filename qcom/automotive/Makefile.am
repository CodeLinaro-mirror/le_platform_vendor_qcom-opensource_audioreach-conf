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

# metadata binary files
metadatabindir = /etc/
metadatabin_DATA = \
    alsalib/sa8797/metadata_bins/A2B_playback_device_md.bin \
    alsalib/sa8797/metadata_bins/A2B_playback_stream_md.bin \
    alsalib/sa8797/metadata_bins/A2B_record_device_md.bin \
    alsalib/sa8797/metadata_bins/A2B_record_stream_device_md.bin \
    alsalib/sa8797/metadata_bins/A2B_record_stream_md.bin \
    alsalib/sa8797/metadata_bins/ADCDevice_md.bin \
    alsalib/sa8797/metadata_bins/ADCStream_device_md.bin \
    alsalib/sa8797/metadata_bins/ADCStream_md.bin \
    alsalib/sa8797/metadata_bins/DACDevice_md.bin \
    alsalib/sa8797/metadata_bins/DACStream_md.bin

endif
