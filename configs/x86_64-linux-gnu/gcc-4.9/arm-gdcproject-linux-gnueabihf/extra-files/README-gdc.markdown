## Introduction
This provides a pre-built, binary [GDC](http://gdcproject.org) toolchain. GDC is a GCC based compiler for the [D language](http://dlang.org).
Sources are available at [github](https://github.com/D-Programming-GDC) and more information is available on the [wiki](http://wiki.dlang.org/GDC). Please
report bugs to our [bugtracker](http://bugzilla.gdcproject.org/).


## Installation
Simply extract this archive to some folder, but do **not extract to your system root folder (/)**.

``` bash
cd /home/jpf
wget http://gdcproject.org/downloads/binaries/x86_64-linux-gnu/arm-linux-gnueabi_2.064.2_gcc4.8.2_665978132e_20140312.tar.xz
tar xf arm-linux-gnueabi_2.064.2_gcc4.8.2_665978132e_20140312.tar.xz
```

### Windows
Extract the archive with your favorite archive manager, e.g. [7zip](http://www.7-zip.org/). If it asks whether it should overwrite files,
answer yes. (The archives are built on case-sensitive filesystems, extracting on case-insensitive filesystems can cause these warnings).


## Usage
### Introduction
The compiler executable is called _TARGET-gdc[.exe]_ and the full path is _TARGET/bin/TARGET-gdc[.exe]_. To compile a simple hello world:

``` bash
echo 'import std.stdio; void main(){writeln("Hello World!");}' > hello.d
arm-gdcproject-linux-gnueabi/bin/arm-gdcproject-linux-gnueabi-gdc hello.d -o hello

#or export the path
export PATH=$PATH:$PWD/arm-gdcproject-linux-gnueabi/bin
arm-gdcproject-linux-gnueabi-gdc hello.d -o hello
```

Windows users should replace arm-gdcproject-linux-gnueabi-gdc with arm-gdcproject-linux-gnueabi-gdc.exe.

More GDC usage information is available at http://wiki.dlang.org/GDC/Using_GDC ,
http://wiki.dlang.org/GDC and http://gdcproject.org .

### Advanced
The difficult part now is how to use third party libraries with cross-compilers.
The standard way to do this is to build all required libraries with this toolchain,
see [crosstool-NG](http://crosstool-ng.org/hg/crosstool-ng/raw-file/tip/docs/5%20-%20Using%20the%20toolchain.txt) for more information.

A simpler way is to use the root filesystems of a real TARGET machine via SSH.
See http://wiki.dlang.org/GDC/Cross_Compiler/Existing_Sysroot for details.
