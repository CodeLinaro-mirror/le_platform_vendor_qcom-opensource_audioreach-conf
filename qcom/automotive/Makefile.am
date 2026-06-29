# No recursion at all
SUBDIRS =

# -------- ALSA (common) --------
alsaconfddir = $(sysconfdir)/alsa/conf.d
alsaconfd_DATA = alsalib/agm.conf

alsaucmvirtdir = $(datadir)/alsa/ucm2/conf.virt.d
alsaucmvirt_DATA = alsalib/agmvirtualsndcard.conf

# -------- gen5 specific --------
if gen5

# ALSA UCM usecase
alsaucmvirt_DATA += \
    alsalib/gen5/agmvirtualsndcard_pp.conf \
    alsalib/gen5/A2BPlayback.conf \
    alsalib/gen5/A2BRecord.conf \
    alsalib/gen5/ADCRecord.conf \
    alsalib/gen5/DACPlayback.conf \
    alsalib/gen5/gain_0.conf \
    alsalib/gen5/gain_2000.conf \
    alsalib/gen5/volume_0.conf \
    alsalib/gen5/volume_15.conf \
    alsalib/gen5/mute.conf \
    alsalib/gen5/unmute.conf

# tinyalsa card definition
carddefdir = $(sysconfdir)
carddef_DATA = tinyalsa/gen5/card-defs.xml

# pkg-config metadata
pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = tinyalsa/gen5/config.pc

# ship template
EXTRA_DIST = tinyalsa/gen5/config.pc.in

# metadata binary files
metadatabindir = /etc/
metadatabin_DATA = \
    alsalib/gen5/metadata_bins/A2B_playback_device_md.bin \
    alsalib/gen5/metadata_bins/A2B_playback_stream_md.bin \
    alsalib/gen5/metadata_bins/A2B_record_device_md.bin \
    alsalib/gen5/metadata_bins/A2B_record_stream_device_md.bin \
    alsalib/gen5/metadata_bins/A2B_record_stream_md.bin \
    alsalib/gen5/metadata_bins/ADCDevice_md.bin \
    alsalib/gen5/metadata_bins/ADCStream_device_md.bin \
    alsalib/gen5/metadata_bins/ADCStream_md.bin \
    alsalib/gen5/metadata_bins/DACDevice_md.bin \
    alsalib/gen5/metadata_bins/DACStream_md.bin \
    alsalib/gen5/metadata_bins/gain_0.bin \
    alsalib/gen5/metadata_bins/gain_2000.bin \
    alsalib/gen5/metadata_bins/volume_0.bin \
    alsalib/gen5/metadata_bins/volume_15.bin \
    alsalib/gen5/metadata_bins/mute.bin \
    alsalib/gen5/metadata_bins/unmute.bin

endif
