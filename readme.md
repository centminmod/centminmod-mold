# mold linker RPM For Centmin Mod LEMP Stack On CentOS 7

* https://github.com/rui314/mold

mold is a faster drop-in replacement for existing Unix linkers - GNU gold, LLVM lld and GNU bfd.

```
yum -q info centmin-mold
Installed Packages
Name        : centmin-mold
Arch        : x86_64
Version     : 1.1
Release     : 1.el7
Size        : 4.0 M
Repo        : installed
From repo   : /centmin-mold-1.1-1.el7.x86_64
Summary     : mold-1.1 for centminmod.com LEMP stack mold-1.1
URL         : https://centminmod.com
License     : unknown
Description : mold-1.1 for centminmod.com LEMP stacks
```

```
rpm -qa centmin-mold --changelog
* Tue Feb 22 2022 George Liu <centminmod.com> 1.1
- mold-1.1 for centminmod.com LEMP stack mold-1.1
```

```
rpm -ql centmin-mold
/usr/local/bin/ld.mold
/usr/local/bin/ld64.mold
/usr/local/bin/mold
/usr/local/lib/mold/mold-wrapper.so
/usr/local/libexec/mold/ld
/usr/local/share/man/man1/mold.1
```

```
readelf -p .comment $(which nginx)

String dump of section '.comment':
  [     0]  GCC: (GNU) 4.8.5 20150623 (Red Hat 4.8.5-44)
  [    2d]  GCC: (GNU) 10.2.1 20210130 (Red Hat 10.2.1-11)
  [    5c]  mold 1.1 (89612b709638b90c8a044e2f96f47d28054ba789; compatible with GNU ld)
```