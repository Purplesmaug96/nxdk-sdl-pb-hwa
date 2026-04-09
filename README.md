
# Simple DirectMedia Layer (SDL) Version 2.0

https://www.libsdl.org/

Simple DirectMedia Layer is a cross-platform development library designed
to provide low level access to audio, keyboard, mouse, joystick, and graphics
hardware via OpenGL and Direct3D. It is used by video playback software,
emulators, and popular games including Valve's award winning catalog
and many Humble Bundle games.

More extensive documentation is available in the docs directory, starting
with README.md

Enjoy!

Sam Lantinga (slouken@libsdl.org)


# Changes

This fork adds a hw-accelerated renderer for the original xbox with NXDK (work done by https://github.com/jroc-hb/nxdk-sdl-pb-hwa), and i have rebased the branch to another person's rebase of nxdk's sdl to sdl2.0.22 (https://github.com/Quantx/nxdk-sdl/tree/nxdk-sdl-2.0.22).

The hw-accelerated renderer doesn't work.

To configure whether to use the hw-accelerated renderer, either comment out the  "#define SDL_VIDEO_RENDER_XBOX_PBKIT" in include/xbox_pbkit_config.h. (its commented out by default)

To use, make it a submodule in your nxdk repo, then build with NXDK_SDL=y make in the nxdk root.