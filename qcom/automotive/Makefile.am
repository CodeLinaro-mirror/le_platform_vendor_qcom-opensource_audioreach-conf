if SA8797
SUBDIRS = sa8797
endif

alsaconfddir = $(sysconfdir)/alsa/conf.d
alsaconfd_DATA = agm.conf

alsaucmvirtdir = $(datadir)/alsa/ucm2/conf.virt.d
alsaucmvirt_DATA = agmvirtualsndcard.conf

alsaucmvirt_DATA += \
    $(SUBDIRS)/A2BPlayback.conf \
    $(SUBDIRS)/A2BRecord.conf \
    $(SUBDIRS)/ADCRecord.conf \
    $(SUBDIRS)/DACPlayback.conf
