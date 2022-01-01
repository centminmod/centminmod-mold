# mold linker RPM For Centmin Mod LEMP Stack On CentOS 7

* https://github.com/rui314/mold

mold is a faster drop-in replacement for existing Unix linkers - GNU gold, LLVM lld and GNU bfd.

```
yum -q info centmin-mold
Installed Packages
Name        : centmin-mold
Arch        : x86_64
Version     : 1.0.1
Release     : 1.el7
Size        : 3.1 M
Repo        : installed
From repo   : /centmin-mold-1.0.1-1.el7.x86_64
Summary     : mold-1.0.1 for centminmod.com LEMP stack mold-1.0.1
URL         : https://centminmod.com
License     : unknown
Description : mold-1.0.1 for centminmod.com LEMP stacks
```

```
rpm -qa centmin-mold --changelog
* Sat Jan 01 2022 George Liu <centminmod.com> 1.0.1
- mold-1.0.1 for centminmod.com LEMP stack mold-1.0.1
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