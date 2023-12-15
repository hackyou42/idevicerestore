AM_CPPFLAGS = -I$(top_srcdir)/include

AM_CFLAGS = \
	$(GLOBAL_CFLAGS) \
	$(LFS_CFLAGS) \
	$(libirecovery_CFLAGS) \
	$(libimobiledevice_CFLAGS) \
	$(libusbmuxd_CFLAGS) \
	$(libplist_CFLAGS) \
	$(limd_glue_CFLAGS) \
	$(libzip_CFLAGS) \
	$(zlib_CFLAGS) \
	$(openssl_CFLAGS) \
	$(libcurl_CFLAGS)

AM_LDFLAGS = \
	$(AC_LDFLAGS) \
	$(libirecovery_LIBS) \
	$(libimobiledevice_LIBS) \
	$(libusbmuxd_LIBS) \
	$(libplist_LIBS) \
	$(limd_glue_LIBS) \
	$(libzip_LIBS) \
	$(zlib_LIBS) \
	$(openssl_LIBS) \
	$(libcurl_LIBS)

AM_LDADD = $(AC_LDADD)

bin_PROGRAMS = idevicerestore

idevicerestore_SOURCES = \
	idevicerestore.c \
	common.c \
	tss.c \
	fls.c \
	mbn.c \
	img3.c \
	img4.c \
	ftab.c \
	ipsw.c \
	normal.c \
	dfu.c \
	recovery.c \
	restore.c \
	asr.c \
	fdr.c \
	limera1n.c \
	download.c  \
	locking.c
    
if USE_INTERNAL_SHA
idevicerestore_SOURCES += sha1.c sha512.c
endif
idevicerestore_CFLAGS = $(AM_CFLAGS)
idevicerestore_LDFLAGS = $(AM_LDFLAGS)
idevicerestore_LDADD = $(AM_LDADD)
