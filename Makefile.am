# Process this file with automake to produce Makefile.in
#
# Add support for the --enable-shared, --disable-shared, --enable-static, --disable-static, --with-pic, and --without-pic configure flags.6 AC_PROG_LIBTOOL and AM_PROG_LIBTOOL are deprecated names for older versions of this macro; autoupdate will upgrade your configure.ac files. 
# https://www.gnu.org/software/libtool/manual/libtool.html#LT_005fINIT
LIBTOOL_DEPS = @LIBTOOL_DEPS@
libtool: $(LIBTOOL_DEPS)
        $(SHELL) ./config.status libtool

AM_CPPFLAGS = -DDATADIR=\"$(pkgdatadir)\"
#
bin_PROGRAMS = arp-scan
#
dist_bin_SCRIPTS = get-oui get-iab arp-fingerprint
#
dist_check_SCRIPTS = check-run1 check-packet check-decode check-host-list
#
dist_man_MANS = arp-scan.1 get-oui.1 get-iab.1 arp-fingerprint.1 mac-vendor.5
#
arp_scan_SOURCES = arp-scan.c arp-scan.h error.c wrappers.c utils.c mt19937ar.c
arp_scan_LDADD = $(LIBOBJS)
#
dist_pkgdata_DATA = ieee-oui.txt ieee-iab.txt mac-vendor.txt
#
TESTS = $(dist_check_SCRIPTS)
EXTRA_DIST = pkt-simple-request.dat pkt-custom-request.dat pkt-custom-request-padding.dat pkt-custom-request-llc.dat pkt-custom-request-vlan.dat pkt-simple-response.pcap pkt-padding-response.pcap pkt-vlan-response.pcap pkt-llc-response.pcap pkt-net1921681-response.pcap pkt-trailer-response.pcap pkt-vlan-llc-response.pcap pkt-custom-request-vlan-llc.dat
