cmake_minimum_required( VERSION 3.4 )

## it's important to not add boost and sdl here-- they're
## handled as parts of the builds for the tools below

add_subdirectory( sdcc )
add_subdirectory( gambatte )

