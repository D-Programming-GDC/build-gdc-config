This repository contains configuration files for the binary toolchain builds
published at http://gdcproject.org/downloads/.

Right now all builds are done using crosstool-NG and a special build-tool which
invokes crosstool-NG. Some paths in the config files are hardcoded and likely
need to be adjusted when not building with the standard VM-image.

The native/cross-native toolchains require patches to crosstool-NG which have not
yet been published.
