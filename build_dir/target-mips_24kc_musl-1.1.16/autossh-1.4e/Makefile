# $Id: Makefile.in,v 1.7 2015/02/10 04:31:16 harding Exp $
#
# Makefile.  Generated from Makefile.in by configure.

VER=		1.4e

SSH=		/usr/bin/ssh

prefix=		/usr
exec_prefix=	/usr
bindir=		/usr/bin
datadir=	/usr/share
mandir=		/usr/man

SRCDIR=		.


CC=		ccache_cc
CFLAGS=		-Os -pipe -mno-branch-likely -mips32r2 -mtune=24kc -fno-caller-saves -fno-plt -fhonour-copts -Wno-error=unused-but-set-variable -Wno-error=unused-result -msoft-float -mips16 -minterlink-mips16 -iremap/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/build_dir/target-mips_24kc_musl-1.1.16/autossh-1.4e:autossh-1.4e -Wformat -Werror=format-security -fstack-protector -D_FORTIFY_SOURCE=1 -Wl,-z,now -Wl,-z,relro  -Wall -DVER=\"$(VER)\" -DSSH_PATH=\"$(SSH)\"
CPPFLAGS=	-I/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/target-mips_24kc_musl-1.1.16/usr/include -I/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/target-mips_24kc_musl-1.1.16/include -I/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/toolchain-mips_24kc_gcc-5.4.0_musl-1.1.16/usr/include -I/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/toolchain-mips_24kc_gcc-5.4.0_musl-1.1.16/include/fortify -I/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/toolchain-mips_24kc_gcc-5.4.0_musl-1.1.16/include 

OFILES=		autossh.o

LD=		@LD@
LDFLAGS=	-L/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/target-mips_24kc_musl-1.1.16/usr/lib -L/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/target-mips_24kc_musl-1.1.16/lib -L/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/toolchain-mips_24kc_gcc-5.4.0_musl-1.1.16/usr/lib -L/home/ubuntu/lede-sdk-17.01.6-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64/staging_dir/toolchain-mips_24kc_gcc-5.4.0_musl-1.1.16/lib -znow -zrelro 
LIBS=		

TARGET=		autossh

all:		$(TARGET)


$(TARGET):	$(OFILES)
		$(CC) $(CPPFLAGS) -o $(TARGET) $(OFILES) $(LIBS)

clean:
		- /bin/rm -f *.o *.a *.core *~

allclean:	clean
		- /bin/rm -f $(TARGET)

distclean:	allclean
		- /bin/rm -f config.log config.cache config.status config.h
		- /bin/rm -rf autom4te.cache
		- /bin/rm -f Makefile

install:	$(TARGET)
		mkdir -p -m 755 $(bindir)
		mkdir -p -m 755 $(prefix)/share/doc/autossh
		mkdir -p -m 755 $(datadir)/examples/autossh
		mkdir -p -m 755 $(mandir)/man1
		cp $(TARGET) $(bindir)
		cp CHANGES README $(datadir)/doc/autossh
		cp autossh.host	$(datadir)/examples/autossh
		cp rscreen $(datadir)/examples/autossh
		cp autossh.1 $(mandir)/man1
		chmod 755 $(bindir)/$(TARGET)
		chmod 644 $(datadir)/doc/autossh/CHANGES
		chmod 644 $(datadir)/doc/autossh/README
		chmod 644 $(datadir)/examples/autossh/autossh.host 
		chmod 644 $(datadir)/examples/autossh/rscreen
		chmod 644 $(mandir)/man1/autossh.1 
