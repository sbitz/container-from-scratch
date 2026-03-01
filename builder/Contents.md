# Contents of Builder Container

## Packages and Software

The following are in the `seed/` directory to enable building in the container

* Autoconf : produces shell scripts that can configure source code.
* Automake : to generate makefiles from a template
* Binutils 
* File : for build scripts
* Findutils : for finding files
* Flex : lexer
* Gawk : GNU Awk
* GCC : GNU C Compiler (and C++)
* GDBM : GNU Database manager library
* Gettext : internationalization lib.
* Glibc : main C library.
* GMP : math libraries.
* Gperf : generates hash function from keys. Required by systemd.
* Grep : search
* Groff : text formatting (man pages)
* Gzip : compression
* Intltool : for I18n from source files
* Libpipeline : Required by Man-DB
* Libtool : library support script for managing shared libraries.
* Libxcrypt** : not itself FIPS compliant. RHEL includes a FIPS compliant version of libgcrypt (can we find that version or another?)
* make : run makefiles
* Man-DB 
* Man-pages 
* Meson : automates the building of software.
* MPC : Supplies arithmetic functions for complex numbers.
* MPFR : Another math library for GCC.
* Ninja : required by Meson 
* Openssl : crypto functions for other packages.
* Patch : modifying or creating files by applying patches (from diff+)
* Perl : used for installation
* Pkgconf : compiler and linker flags
* Sed : used during configuration
* Tar : for unpacking files
* Tcl : Tool Command Language for test suites 
* Texinfo : read, write, and convert info pages.
* XML::Parser : Perl module for working with Expat 
* XZ Utils : compression and decompression utility.
* Zlib : compression and decompression.
* Zstd : compression and decompression.

----

Also from LFS 

* Acl 
* Attr 
* Bash 
* Bc : arbitrary precision numeric processing language
* Bison
* Bzip2
* Check
* Coreutils
* D-Bus 
* DejaGNU
* Diffutils 
* E2fsprogs
* Expat
* Expect 
* GRUB 
* Iana-etc  - network capabilities - provided by Docker?
* Inetutils - network administration - probably provided by Docker
* IProute2 : for networking - possibly provided by Docker
* Jinja2 : python templating
* Kbd : key-table files for non-US keyboards 
* Kmod : administration of Linux kernel modules 
* Less : for scrolling through output. Omit since we don't plan to include a shell.
* Libcap : userspace interfaces
* Libelf : for building the kernel 
* Libffi : runtime tool for some programs. Not sure if it is needed
* M4
* MarkupSafe : python module for processing strings, required for Jinja.
* Ncurses : libraries for terminal cursors.
* Procps-NG : process monitoring
* Psmisc : information about running processes. Possibly provided by Docker.
* Python 3 : not needed unless for building other software.
* Readline : not including a shell
* Shadow : used for passwords - not sure if it is needed.
* Util-linux : miscellaneous utility programs.
* Vim : not including a shell 
* Wheel : not including python

--- 

We will likely need


* Entropy - track and add entropy to the container. Map from host if needed.
* git : to pull down packages for compliation and installation


