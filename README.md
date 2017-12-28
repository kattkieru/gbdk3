gbdk3

Gameboy Development Kit v3
==========================

If you got here through some search, I apologize, but this is not as exciting as you were thinking.

If you want to tinker, do:

```bash
git clone https://github.com/kattkieru/gbdk3.git --recursive
mkdir build
cd build
cmake -G "Unix Makefiles" ..
make -j 8 install
```

The important subrepos:

gambatte: bootstrap build of gambatte-sdl (macOS only for now). This is now configured to install the gambatte binary into gbdk3/bin.

sdcc: bootstrap build of the SDCC compiler toolchain for Gameboy (macOS only for now). This bootstrap disables support for other chipsets in sdcc.

gbdk3_stdlib: Fork of the gbdk-n repo by Andreas Karlsson. I'll integrate the build for this when I have time.

Possibly interesting to you:
https://github.com/kattkieru/atmd -- Fork of the original Affinix Tile/Map Designer (win32 only). I embedded SDL 1.2.15 and made the build work.  It's not in this repo because A) I haven't yet figured out how to use it; and B) it's for Windows only, which is not where I do my real work.

More is coming, but there is no timeline.

~ k

