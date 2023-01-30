
## Compiler environment

In addition to CodeBlocks, MinGW-w64 with threading support needs to be installed separately. Do not use the default MinGW that is shipped with CodeBlocks.
This guide assumes using the 32 bit MinGW-w64 version for the builds. It is also easier to use Git Bash environment for command line tasks.
It is recommended to use the default "GNU GCC compiler" profile in CodeBlocks for this since `glsmac.cbp` project file also assumes using this compiler for the project.

After extracting the files, MinGW-w64 toolkit paths and filenames have to be entered in CodeBlocks config in Settings > Compiler.
This can be configured by adjusting the filenames in Toolchain Executables tab. If using the 64 bit MinGW version, some filenames may slightly change,
and you might also have to manually adjust the linked libraries from `glsmac.cbp` project file.

* [CodeBlocks](https://www.codeblocks.org/downloads/binaries/)
* [MinGW 32 bit](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/8.1.0/threads-posix/dwarf/i686-8.1.0-release-posix-dwarf-rt_v6-rev0.7z)
* [MinGW 64 bit](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/8.1.0/threads-posix/seh/x86_64-8.1.0-release-posix-seh-rt_v6-rev0.7z)


## Library sources

* [SDL](https://github.com/libsdl-org/SDL/releases/download/release-2.26.2/SDL2-devel-2.26.2-mingw.zip)
* [SDL_image](https://github.com/libsdl-org/SDL_image/releases/download/release-2.6.2/SDL2_image-devel-2.6.2-mingw.zip)
* [Freetype](https://download.savannah.gnu.org/releases/freetype/ft2121.zip)
* [Freeglut](files/freeglut-MinGW-3.0.0-1.mp.zip)
* [Glew](https://github.com/nigels-com/glew/releases/download/glew-2.2.0/glew-2.2.0.zip)


## Install libraries

With the exception of Freeglut, these libraries need to be separately compiled using the MinGW-w64 environment that was configured previously.
After compiling, these extra files should be extracted to the main MinGW i686 or x86_64 folder (these paths are relative to the destination).

    include/GL/eglew.h
    include/GL/freeglut.h
    include/GL/freeglut_ext.h
    include/GL/freeglut_std.h
    include/GL/glew.h
    include/GL/glut.h
    include/GL/glxew.h
    include/GL/wglew.h
    include/SDL.h
    include/SDL_assert.h
    include/SDL_atomic.h
    include/SDL_audio.h
    include/SDL_bits.h
    include/SDL_blendmode.h
    include/SDL_clipboard.h
    include/SDL_config.h
    include/SDL_cpuinfo.h
    include/SDL_egl.h
    include/SDL_endian.h
    include/SDL_error.h
    include/SDL_events.h
    include/SDL_filesystem.h
    include/SDL_gamecontroller.h
    include/SDL_gesture.h
    include/SDL_guid.h
    include/SDL_haptic.h
    include/SDL_hidapi.h
    include/SDL_hints.h
    include/SDL_image.h
    include/SDL_joystick.h
    include/SDL_keyboard.h
    include/SDL_keycode.h
    include/SDL_loadso.h
    include/SDL_locale.h
    include/SDL_log.h
    include/SDL_main.h
    include/SDL_messagebox.h
    include/SDL_metal.h
    include/SDL_misc.h
    include/SDL_mouse.h
    include/SDL_mutex.h
    include/SDL_name.h
    include/SDL_opengl.h
    include/SDL_opengl_glext.h
    include/SDL_opengles.h
    include/SDL_opengles2.h
    include/SDL_opengles2_gl2.h
    include/SDL_opengles2_gl2ext.h
    include/SDL_opengles2_gl2platform.h
    include/SDL_opengles2_khrplatform.h
    include/SDL_pixels.h
    include/SDL_platform.h
    include/SDL_power.h
    include/SDL_quit.h
    include/SDL_rect.h
    include/SDL_render.h
    include/SDL_revision.h
    include/SDL_rwops.h
    include/SDL_scancode.h
    include/SDL_sensor.h
    include/SDL_shape.h
    include/SDL_stdinc.h
    include/SDL_surface.h
    include/SDL_system.h
    include/SDL_syswm.h
    include/SDL_test.h
    include/SDL_test_assert.h
    include/SDL_test_common.h
    include/SDL_test_compare.h
    include/SDL_test_crc32.h
    include/SDL_test_font.h
    include/SDL_test_fuzzer.h
    include/SDL_test_harness.h
    include/SDL_test_images.h
    include/SDL_test_log.h
    include/SDL_test_md5.h
    include/SDL_test_memory.h
    include/SDL_test_random.h
    include/SDL_thread.h
    include/SDL_timer.h
    include/SDL_touch.h
    include/SDL_types.h
    include/SDL_version.h
    include/SDL_video.h
    include/SDL_vulkan.h
    include/begin_code.h
    include/close_code.h
    include/dlg/dlg.h
    include/dlg/output.h
    include/freetype/config/ftconfig.h
    include/freetype/config/ftheader.h
    include/freetype/config/ftmodule.h
    include/freetype/config/ftoption.h
    include/freetype/config/ftstdlib.h
    include/freetype/config/integer-types.h
    include/freetype/config/mac-support.h
    include/freetype/config/public-macros.h
    include/freetype/freetype.h
    include/freetype/ftadvanc.h
    include/freetype/ftbbox.h
    include/freetype/ftbdf.h
    include/freetype/ftbitmap.h
    include/freetype/ftbzip2.h
    include/freetype/ftcache.h
    include/freetype/ftchapters.h
    include/freetype/ftcid.h
    include/freetype/ftcolor.h
    include/freetype/ftdriver.h
    include/freetype/fterrdef.h
    include/freetype/fterrors.h
    include/freetype/ftfntfmt.h
    include/freetype/ftgasp.h
    include/freetype/ftglyph.h
    include/freetype/ftgxval.h
    include/freetype/ftgzip.h
    include/freetype/ftimage.h
    include/freetype/ftincrem.h
    include/freetype/ftlcdfil.h
    include/freetype/ftlist.h
    include/freetype/ftlogging.h
    include/freetype/ftlzw.h
    include/freetype/ftmac.h
    include/freetype/ftmm.h
    include/freetype/ftmodapi.h
    include/freetype/ftmoderr.h
    include/freetype/ftotval.h
    include/freetype/ftoutln.h
    include/freetype/ftparams.h
    include/freetype/ftpfr.h
    include/freetype/ftrender.h
    include/freetype/ftsizes.h
    include/freetype/ftsnames.h
    include/freetype/ftstroke.h
    include/freetype/ftsynth.h
    include/freetype/ftsystem.h
    include/freetype/fttrigon.h
    include/freetype/fttypes.h
    include/freetype/ftwinfnt.h
    include/freetype/internal/autohint.h
    include/freetype/internal/cffotypes.h
    include/freetype/internal/cfftypes.h
    include/freetype/internal/compiler-macros.h
    include/freetype/internal/ftcalc.h
    include/freetype/internal/ftdebug.h
    include/freetype/internal/ftdrv.h
    include/freetype/internal/ftgloadr.h
    include/freetype/internal/fthash.h
    include/freetype/internal/ftmemory.h
    include/freetype/internal/ftobjs.h
    include/freetype/internal/ftpsprop.h
    include/freetype/internal/ftrfork.h
    include/freetype/internal/ftserv.h
    include/freetype/internal/ftstream.h
    include/freetype/internal/fttrace.h
    include/freetype/internal/ftvalid.h
    include/freetype/internal/psaux.h
    include/freetype/internal/pshints.h
    include/freetype/internal/services/svbdf.h
    include/freetype/internal/services/svcfftl.h
    include/freetype/internal/services/svcid.h
    include/freetype/internal/services/svfntfmt.h
    include/freetype/internal/services/svgldict.h
    include/freetype/internal/services/svgxval.h
    include/freetype/internal/services/svkern.h
    include/freetype/internal/services/svmetric.h
    include/freetype/internal/services/svmm.h
    include/freetype/internal/services/svotval.h
    include/freetype/internal/services/svpfr.h
    include/freetype/internal/services/svpostnm.h
    include/freetype/internal/services/svprop.h
    include/freetype/internal/services/svpscmap.h
    include/freetype/internal/services/svpsinfo.h
    include/freetype/internal/services/svsfnt.h
    include/freetype/internal/services/svttcmap.h
    include/freetype/internal/services/svtteng.h
    include/freetype/internal/services/svttglyf.h
    include/freetype/internal/services/svwinfnt.h
    include/freetype/internal/sfnt.h
    include/freetype/internal/svginterface.h
    include/freetype/internal/t1types.h
    include/freetype/internal/tttypes.h
    include/freetype/internal/wofftypes.h
    include/freetype/otsvg.h
    include/freetype/t1tables.h
    include/freetype/ttnameid.h
    include/freetype/tttables.h
    include/freetype/tttags.h
    include/ft2build.h
    lib/glew32.dll
    lib/glew32mx.dll
    lib/libSDL2.a
    lib/libSDL2.dll.a
    lib/libSDL2.la
    lib/libSDL2_image.a
    lib/libSDL2_image.dll.a
    lib/libSDL2_image.la
    lib/libSDL2_test.a
    lib/libSDL2_test.la
    lib/libSDL2main.a
    lib/libSDL2main.la
    lib/libfreeglut.a
    lib/libfreeglut_static.a
    lib/libfreetype.a
    lib/libglew32.a
    lib/libglew32.dll.a
    lib/libglew32mx.a
    lib/libglew32mx.dll.a


## Compile glsmac project

After the dependencies are installed, copy `glsmac.cbp` project file to the glsmac project folder and recursively add all files from `src`
to the project in case the cbp project file is missing something. The project should now compile from CodeBlocks interface.

