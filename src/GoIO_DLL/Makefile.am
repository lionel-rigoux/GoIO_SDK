AM_CXXFLAGS = $(GIO_EXTRA_CFLAGS)
AM_CFLAGS = $(GIO_EXTRA_CFLAGS)

INCLUDES = -I$(top_srcdir) -I$(top_srcdir)/GoIO_cpp/ -I$(top_srcdir)/GoIO_cpp/Linux/ -I$(top_srcdir)/GoIO_DLL/

EXTRA_DIST = GoIO.pc.in 48-ldusb.rules vstlibusb.rules

library_includedir= $(includedir)/GoIO
library_include_HEADERS = GoIO_DLL_interface.h

lib_LTLIBRARIES = libGoIO.la

libGoIO_la_SOURCES = GoIO_DLL_interface.cpp

libGoIO_la_LIBADD= $(top_srcdir)/GoIO_cpp/libGoIOcpp.la $(top_srcdir)/GoIO_cpp/Linux/libGoIOcppLinux.la -lusb-1.0

libGoIO_la_LDFLAGS = -version-info 2:53:0

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = GoIO.pc

udevdir = $(sysconfdir)/udev/rules.d
dist_udev_DATA = 48-ldusb.rules vstlibusb.rules
