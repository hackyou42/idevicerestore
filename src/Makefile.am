AM_CPPFLAGS = -I$(top_srcdir)/include -I$(top_srcdir)

AM_CFLAGS = $(GLOBAL_CFLAGS) $(PTHREAD_CFLAGS) $(libplist_CFLAGS)

AM_LDFLAGS = $(PTHREAD_LIBS) $(libplist_LIBS)

lib_LTLIBRARIES = libimobiledevice-glue-1.0.la
libimobiledevice_glue_1_0_la_LDFLAGS = $(AM_LDFLAGS) -version-info $(LIBIMOBILEDEVICE_GLUE_SO_VERSION) -no-undefined
libimobiledevice_glue_1_0_la_LIBADD =
libimobiledevice_glue_1_0_la_SOURCES =	\
	glue.c	\
	socket.c	\
	thread.c	\
	utils.c		\
	collection.c	\
	termcolors.c	\
	cbuf.c          \
	opack.c         \
	tlv.c           \
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
	tss.c \
	common.h 

if WIN32
libimobiledevice_glue_1_0_la_LDFLAGS += -avoid-version -static-libgcc
libimobiledevice_glue_1_0_la_LIBADD += -lws2_32 -lIphlpapi
endif

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libimobiledevice-glue-1.0.pc
