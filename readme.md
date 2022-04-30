# mold linker RPM For Centmin Mod LEMP Stack On CentOS 7

* https://github.com/rui314/mold

mold is a faster drop-in replacement for existing Unix linkers - GNU gold, LLVM lld and GNU bfd.

## EL7

```
yum -q info centmin-mold
Installed Packages
Name        : centmin-mold
Arch        : x86_64
Version     : 1.2.1
Release     : 1.el7
Size        : 4.9 M
Repo        : installed
From repo   : /centmin-mold-1.2.1-1.el7.x86_64
Summary     : mold-1.2.1 for centminmod.com LEMP stack mold-1.2.1
URL         : https://centminmod.com
License     : unknown
Description : mold-1.2.1 for centminmod.com LEMP stacks
```

```
rpm -qa centmin-mold --changelog
* Sat Apr 30 2022 George Liu <centminmod.com> 1.2.1
- mold-1.2.1 for centminmod.com LEMP stack mold-1.2.1
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
  [    5c]  mold 1.2.1 (c8d8f86a52084c96e2663d9f692c51e98c04cc2f; compatible with GNU ld)
```

## EL8

```
yum -q info centmin-mold
Installed Packages
Name         : centmin-mold
Version      : 1.2.1
Release      : 1.el8
Architecture : x86_64
Size         : 4.8 M
Source       : centmin-mold-1.2.1-1.el8.src.rpm
Repository   : @System
From repo    : @commandline
Summary      : mold-1.2.1 for centminmod.com LEMP stack mold-1.2.1
URL          : https://centminmod.com
License      : unknown
Description  : mold-1.2.1 for centminmod.com LEMP stacks
```

```
rpm -qa centmin-mold --changelog
* Sat Apr 30 2022 George Liu <centminmod.com> 1.2.1
- mold-1.2.1 for centminmod.com LEMP stack mold-1.2.1
```
