# Kroma Desktop releases

Official binary-only releases for Kroma Desktop by Quivr.

This public repository contains installers and the release workflow only. Application source remains private in `Quivr-stream/kroma-desktop`. Windows x64, macOS Apple Silicon, macOS Intel, and Linux x64 bundles are built from a pinned private source revision. Linux builds use Ubuntu 22.04 and provide AppImage and Debian (`.deb`) packages. ARM Linux, Flatpak and RPM are not built yet.

Artifacts accumulate in a draft release; publication happens only after all four platform builds succeed. Preview releases do not replace the stable updater release. Linux AppImage in-place updates require a writable AppImage location; Debian installations are updated with the system package manager. A successful build is not proof of runtime compatibility on every Linux distribution or desktop environment.
