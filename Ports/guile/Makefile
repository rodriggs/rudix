BuildRequires += $(LibDir)/libgmp.la	# static-gmp
BuildRequires += $(LibDir)/libintl.la	# static-gettext
BuildRequires += $(LibDir)/libltdl.la	# static-libtool

include ../../Library/GNU.mk

Title=		GNU Guile
Name=		guile
Version=	1.8.8
Revision=	3
Site=		https://www.gnu.org/software/guile/
Source=		https://ftp.gnu.org/gnu/guile/guile-$(Version).tar.gz
License=	LGPLv2

LicenseFile=	$(SourceDir)/LICENSE

EnvExtra += 	LIBFFI_CFLAGS="-I/usr/include/ffi"
EnvExtra +=	LIBFFI_LIBS="-L/usr/local/lib -lffi"

ifeq ($(RUDIX_BUILD_WITH_STATIC_LIBS),yes)
LdFlags += -framework CoreFoundation -liconv
endif

define install_post_hook
install -m 644 $(SourceDir)/{GUILE-Version,HACKING} $(InstallDir)/$(DocDir)/$(Name)
endef

define final_post_hook
$(BinDir)/guile -v | grep $(Version)
endef

ifeq ($(OSXVersion),10.6)
RUDIX_UNIVERSAL=no
endif
