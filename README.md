Gameboy Development Kit v3
==========================

This repo is a collection of tools for creating Gameboy games.  I've been tinkering away with some older tools and trying to package everything together in one easy-to-build place.  Most of what I've added here is just CMakeLists.txt files.

If you got here through some search, I apologize, but this is probably not as exciting as you were thinking.

If you want to tinker, do:

```bash
git clone https://github.com/kattkieru/gbdk3.git --recursive
mkdir build
cd build
cmake -G "Unix Makefiles" ..
make -j 8 install
```

To test a built cartridge:
```bash
bin/gambatte --scale 3 -y /path/to/some_cart.gb
```

If you don't use the `-y` flag, the colors may be screwed up. No idea why yet; for now the workaround is good enough.

Important Subrepos
------------------

*gambatte*: bootstrap build of gambatte-sdl (macOS 32bit only for now). This is configured to install the gambatte binary into gbdk3/bin.

*sdcc*: bootstrap build of the SDCC compiler toolchain for Gameboy (macOS only for now). This bootstrap disables support for other chipsets in sdcc.  This is configured to install the sdcc binaries into gbdk3/bin.

*gbdk3_stdlib*: Fork of the gbdk-n repo by Andreas Karlsson. I'll integrate the build for this when I have time.

Possibly interesting to you:

*https://github.com/kattkieru/atmd* -- Fork of the original _Affinix Tile/Map Designer_ (win32 only). I embedded SDL 1.2.15 and made the build work.  It's not in this repo because A) I haven't yet figured out how to use it; and B) it's for Windows only, which is not where I do my real work.

More is coming, but there is no timeline.  This is a hobby.  Pull requests are welcome.


Note On Building Larger Cartridges:
-----------------------------------

The crt0 file that comes in gbdk3_stdlib is locked to a small size. If you want to change the size of the rom or the type of MBC, I think you'll need to copy crt0.s into your project and make the appropriate changes.  As far as I know recent versions of SDCC can handle the banked link, but I haven't had time to test it yet.

~ kiki

