include ../../Library/GNU.mk

Title=		GNU Screen
Name=		screen
Version=	4.4.0
Revision=	0
Site=		http://www.gnu.org/software/screen/
Source=		http://ftp.gnu.org/gnu/screen//$(Name)-$(Version).tar.gz
License=	GPLv3

GnuConfigureExtra += --with-sys-screenrc=/usr/local/etc
GnuConfigureExtra += -enable-telnet

define test_inner_hook
$(BinDir)/screen --version | grep 'Screen version'
endef
