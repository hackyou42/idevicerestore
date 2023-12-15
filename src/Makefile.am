AM_CPPFLAGS = -I$(top_srcdir)/include -I$(top_srcdir)

AM_CFLAGS = $(GLOBAL_CFLAGS) $(PTHREAD_CFLAGS) $(libplist_CFLAGS)

AM_LDFLAGS = $(PTHREAD_LIBS) $(libplist_LIBS)

lib_LTLIBRARIES = idevicerestore.la
idevicerestore_LDFLAGS = $(AM_LDFLAGS) -version-info $(IDEVICERESTORE_SO_VERSION) -no-undefined
idevicerestore_LIBADD =
idevicerestore_SOURCES =	\
	asr.c \
	common.c \
	dfu.c \
	download.c \
	fdr.c \
	fls.c \
	ftab.c \
	idevicerestore.c \
	img3.c \
	img4.c \
	ipsw.c \
	limera1n.c \
	locking.c \
	mbn.c \
	normal.c \
	recovery.c \
	restore.c \
	sha1.c \
	sha512.c \
	tss.c

if WIN32
idevicerestore_LDFLAGS += -avoid-version -static-libgcc
idevicerestore_LIBADD += -lws2_32 -lIphlpapi
endif

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = idevicerestore.pc
