include ../../Library/Unix.mk

Title=		Redis
Name=		redis
Version=	3.0.3
Revision=	0
Site=		http://redis.io/
Source=		http://download.redis.io/releases/$(Name)-$(Version).tar.gz
License=	BSD

BuildDir=	$(SourceDir)/src

MakeExtra += ARCH="$(LdFlags)" CCLINK="$(LdFlags)"
MakeInstallExtra += PREFIX=$(PortDir)/$(InstallDir)/$(Prefix)

define test_inner_hook
$(BinDir)/redis-cli -v | grep $(Version)
$(BinDir)/redis-server --version | grep $(Version)
endef
