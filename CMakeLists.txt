cmake_minimum_required( VERSION 3.4 )

## it's important to not add boost and sdl here-- they're
## handled as parts of the builds for the tools below

## compiler suite
add_subdirectory( sdcc )

## bank-aware linker
add_subdirectory( aslink-gb )

## excellent, accurate emulator
add_subdirectory( gambatte )

