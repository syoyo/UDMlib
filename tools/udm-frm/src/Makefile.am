#
# udm-frm (File Rank Mapper for UDMlib)
# Copyright (C) 2012-2015 Institute of Industrial Science, The University of Tokyo.
# All rights reserved.
#

bin_PROGRAMS = udm-frm

AM_CPPFLAGS = -I$(top_builddir)/include \
           -I$(top_builddir)/tools/udm-frm/include

AM_CXXFLAGS = @MPICH_FLAGS@ @CGNS_FLAGS@ @TP_FLAGS@  @ZOLTAN_FLAGS@  @UDM_FLAGS@
AM_LDFLAGS = @UDM_LDFLAGS@ @ZOLTAN_LDFLAGS@ @CGNS_LDFLAGS@ @MPICH_LDFLAGS@
LDADD = @UDM_LIBS@ @ZOLTAN_LIBS@ @CGNS_LIBS@ @MPICH_LIBS@ @TP_LDFLAGS@

udm_frm_SOURCES = \
    UdmStaging.cpp \
    udm_frm.cpp
    
udm_frm_includedir = $(includedir)
udm_frm_include_HEADERS = \
    $(top_builddir)/tools/udm-frm/include/UdmStaging.h \
    $(top_builddir)/tools/udm-frm/include/udmfrm_version.h

all-local:
	mkdir -p $(top_builddir)/bin
	cp $(bin_PROGRAMS) $(top_builddir)/bin/

clean-local:
	rm -f $(top_builddir)/bin/$(bin_PROGRAMS)
	rm -rf $(top_builddir)/bin
