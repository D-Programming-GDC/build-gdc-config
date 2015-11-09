## Introduction
This package provides a pre-built, binary [GDC](http://gdcproject.org) toolchain. GDC is a GCC based compiler for the [D language](http://dlang.org).
Sources are available on [github](https://github.com/D-Programming-GDC) and more information is available on the [wiki](http://wiki.dlang.org/GDC). Please
report bugs to our [bugtracker](http://bugzilla.gdcproject.org/).

This package is only an addon to the devkitPPC toolchain. devkitPPC is part of the [devkitPro](https://devkitpro.org/) project
and compiles code for PowerPC based video game consoles, such as the Gamecube and Wii consoles.


## Installation
First install a complete [devkitPPC](https://devkitpro.org/) toolchain as explained on [devkitPro.org](http://devkitpro.org/wiki/Getting_Started).
Make sure the installed devkitPPC revision matches the revision used for this package. The revision is part of this package's file name (e.g. _r27_).
Then simply extract this archive to the _devkitPro_ root folder.


## Usage
The compiler executable is called _powerpc-eabi-gdc[.exe]_ and it is in the _devkitPPC/bin_ folder. This package does
currently not include druntime or phobos libraries.

This package may include an updated gdb debugger in the _devkitPPC/gdb-X.Y_ folder where X.Y is the gdb version. Add the
_devkitPPC/gdb-X.Y/bin_ folder to the _PATH_ environment variable to use this gdb version.

More GDC usage information is available at http://wiki.dlang.org/GDC/Using_GDC ,
http://wiki.dlang.org/GDC and http://gdcproject.org .
