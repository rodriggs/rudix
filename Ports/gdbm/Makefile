include ../../Library/GNU.mk

Title=		GNU dbm
Name=		gdbm
Version=	1.11
Revision=	0
Site=		http://www.gnu.org.ua/software/gdbm/
Source=		ftp://ftp.gnu.org/gnu/gdbm/$(Name)-$(Version).tar.gz
License=	GPL

define test_inner_hook
$(BinDir)/gdbm_dump --version | grep $(Version)
$(BinDir)/gdbm_load --version | grep $(Version)
$(BinDir)/gdbmtool --version | grep $(Version)
endef
