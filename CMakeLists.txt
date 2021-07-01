cmake_minimum_required(VERSION 3.19)
project(agmod)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

include_directories(common)
include_directories(dlls)
include_directories(engine)
include_directories(external/SDL2)
include_directories(game_shared)
include_directories(game_shared/bot)
include_directories(ministl)
include_directories(pm_shared)
include_directories(public)
include_directories(public/cl_dll)
include_directories(public/steam)

add_executable(agmod
        dlls/wpn_shared/hl_wpn_glock.cpp
        dlls/activity.h
        dlls/activitymap.h
        dlls/aflock.cpp
        dlls/agadmin.cpp
        dlls/agadmin.h
        dlls/agadmincache.cpp
        dlls/agadmincache.h
        dlls/agarena.cpp
        dlls/agarena.h
        dlls/agclient.cpp
        dlls/agclient.h
        dlls/agcommand.cpp
        dlls/agcommand.h
        dlls/agctf.cpp
        dlls/agctf.h
        dlls/agdom.cpp
        dlls/agdom.h
        dlls/aggame.cpp
        dlls/aggame.h
        dlls/aggamemode.cpp
        dlls/aggamemode.h
        dlls/aggamerules.cpp
        dlls/aggamerules.h
        dlls/agglobal.cpp
        dlls/agglobal.h
        dlls/aginfointermission.cpp
        dlls/aginfointermission.h
        dlls/aglms.cpp
        dlls/aglms.h
        dlls/agmatch.cpp
        dlls/agmatch.h
        dlls/agrunt.cpp
        dlls/agscore.cpp
        dlls/agscore.h
        dlls/agscorecache.cpp
        dlls/agscorecache.h
        dlls/agscorelog.cpp
        dlls/agscorelog.h
        dlls/agsettings.cpp
        dlls/agsettings.h
        dlls/agspectator.cpp
        dlls/agstats.cpp
        dlls/agstats.h
        dlls/agsuddendeath.cpp
        dlls/agsuddendeath.h
        dlls/agtimeout.cpp
        dlls/agtimeout.h
        dlls/agtimer.cpp
        dlls/agtimer.h
        dlls/agvote.cpp
        dlls/agvote.h
        dlls/agwallhack.cpp
        dlls/agwallhack.h
        dlls/airtank.cpp
        dlls/animating.cpp
        dlls/animation.cpp
        dlls/animation.h
        dlls/apache.cpp
        dlls/barnacle.cpp
        dlls/barney.cpp
        dlls/basemonster.h
        dlls/bigmomma.cpp
        dlls/bloater.cpp
        dlls/bmodels.cpp
        dlls/bullsquid.cpp
        dlls/buttons.cpp
        dlls/cbase.cpp
        dlls/cbase.h
        dlls/cdll_dll.h
        dlls/client.cpp
        dlls/client.h
        dlls/combat.cpp
        dlls/controller.cpp
        dlls/crossbow.cpp
        dlls/crowbar.cpp
        dlls/decals.h
        dlls/defaultai.cpp
        dlls/defaultai.h
        dlls/doors.cpp
        dlls/doors.h
        dlls/effects.cpp
        dlls/effects.h
        dlls/egon.cpp
        dlls/enginecallback.h
        dlls/explode.cpp
        dlls/explode.h
        dlls/extdll.h
        dlls/flyingmonster.cpp
        dlls/flyingmonster.h
        dlls/func_break.cpp
        dlls/func_break.h
        dlls/func_tank.cpp
        dlls/game.cpp
        dlls/game.h
        dlls/gamerules.cpp
        dlls/gamerules.h
        dlls/gargantua.cpp
        dlls/gauss.cpp
        dlls/genericmonster.cpp
        dlls/ggrenade.cpp
        dlls/globals.cpp
        dlls/gman.cpp
        dlls/h_ai.cpp
        dlls/h_battery.cpp
        dlls/h_cine.cpp
        dlls/h_cycler.cpp
        dlls/h_export.cpp
        dlls/handgrenade.cpp
        dlls/hassassin.cpp
        dlls/headcrab.cpp
        dlls/healthkit.cpp
        dlls/hgrunt.cpp
        dlls/hornet.cpp
        dlls/hornet.h
        dlls/hornetgun.cpp
        dlls/houndeye.cpp
        dlls/ichthyosaur.cpp
        dlls/islave.cpp
        dlls/items.cpp
        dlls/items.h
        dlls/leech.cpp
        dlls/lights.cpp
        dlls/maprules.cpp
        dlls/maprules.h
        dlls/monsterevent.h
        dlls/monstermaker.cpp
        dlls/monsters.cpp
        dlls/monsters.h
        dlls/monsterstate.cpp
        dlls/mortar.cpp
        dlls/mp5.cpp
        dlls/multiplay_gamerules.cpp
        dlls/multiplay_gamerules.h
        dlls/nihilanth.cpp
        dlls/nodes.cpp
        dlls/nodes.h
        dlls/observer.cpp
        dlls/osprey.cpp
        dlls/pathcorner.cpp
        dlls/plane.cpp
        dlls/plane.h
        dlls/plats.cpp
        dlls/player.cpp
        dlls/player.h
        dlls/playermonster.cpp
        dlls/python.cpp
        dlls/rat.cpp
        dlls/roach.cpp
        dlls/rpg.cpp
        dlls/satchel.cpp
        dlls/saverestore.h
        dlls/schedule.cpp
        dlls/schedule.h
        dlls/scientist.cpp
        dlls/scripted.cpp
        dlls/scripted.h
        dlls/scriptevent.h
        dlls/shotgun.cpp
        dlls/singleplay_gamerules.cpp
        dlls/singleplay_gamerules.h
        dlls/skill.cpp
        dlls/skill.h
        dlls/sound.cpp
        dlls/soundent.cpp
        dlls/soundent.h
        dlls/spawnchooser.cpp
        dlls/spawnchooser.h
        dlls/spectator.cpp
        dlls/spectator.h
        dlls/squad.h
        dlls/squadmonster.cpp
        dlls/squadmonster.h
        dlls/squeakgrenade.cpp
        #dlls/stats.cpp
        dlls/subs.cpp
        dlls/talkmonster.cpp
        dlls/talkmonster.h
        dlls/teamplay_gamerules.cpp
        dlls/teamplay_gamerules.h
        dlls/tempmonster.cpp
        dlls/tentacle.cpp
        dlls/trains.h
        dlls/triggers.cpp
        dlls/tripmine.cpp
        dlls/turret.cpp
        dlls/util.cpp
        dlls/util.h
        dlls/vector.h
        dlls/weapons.cpp
        dlls/weapons.h
        dlls/world.cpp
        dlls/xen.cpp
        dlls/zombie.cpp
        engine/anorms.h
        engine/APIProxy.h
        engine/cdll_int.h
        engine/custom.h
        engine/customentity.h
        engine/edict.h
        engine/eiface.h
        engine/progdefs.h
        engine/progs.h
        engine/shake.h
        engine/studio.h
        external/SDL2/begin_code.h
        external/SDL2/close_code.h
        external/SDL2/merge_sdl2.sh
        external/SDL2/SDL.h
        external/SDL2/SDL_assert.h
        external/SDL2/SDL_atomic.h
        external/SDL2/SDL_audio.h
        external/SDL2/SDL_bits.h
        external/SDL2/SDL_blendmode.h
        external/SDL2/SDL_clipboard.h
        external/SDL2/SDL_config.h
        external/SDL2/SDL_config_android.h
        external/SDL2/SDL_config_iphoneos.h
        external/SDL2/SDL_config_macosx.h
        external/SDL2/SDL_config_minimal.h
        external/SDL2/SDL_config_nintendods.h
        external/SDL2/SDL_config_pandora.h
        external/SDL2/SDL_config_windows.h
        external/SDL2/SDL_config_wiz.h
        external/SDL2/SDL_copying.h
        external/SDL2/SDL_cpuinfo.h
        external/SDL2/SDL_endian.h
        external/SDL2/SDL_error.h
        external/SDL2/SDL_events.h
        external/SDL2/SDL_gamecontroller.h
        external/SDL2/SDL_gesture.h
        external/SDL2/SDL_haptic.h
        external/SDL2/SDL_hints.h
        external/SDL2/SDL_input.h
        external/SDL2/SDL_joystick.h
        external/SDL2/SDL_keyboard.h
        external/SDL2/SDL_keycode.h
        external/SDL2/SDL_loadso.h
        external/SDL2/SDL_log.h
        external/SDL2/SDL_main.h
        external/SDL2/SDL_messagebox.h
        external/SDL2/SDL_mouse.h
        external/SDL2/SDL_mutex.h
        external/SDL2/SDL_name.h
        external/SDL2/SDL_opengl.h
        external/SDL2/SDL_opengles.h
        external/SDL2/SDL_opengles2.h
        external/SDL2/SDL_pixels.h
        external/SDL2/SDL_platform.h
        external/SDL2/SDL_power.h
        external/SDL2/SDL_quit.h
        external/SDL2/SDL_rect.h
        external/SDL2/SDL_render.h
        external/SDL2/SDL_revision.h
        external/SDL2/SDL_rwops.h
        external/SDL2/SDL_scancode.h
        external/SDL2/SDL_shape.h
        external/SDL2/SDL_stdinc.h
        external/SDL2/SDL_surface.h
        external/SDL2/SDL_system.h
        external/SDL2/SDL_syswm.h
        external/SDL2/SDL_test.h
        external/SDL2/SDL_test_assert.h
        external/SDL2/SDL_test_common.h
        external/SDL2/SDL_test_compare.h
        external/SDL2/SDL_test_crc32.h
        external/SDL2/SDL_test_font.h
        external/SDL2/SDL_test_fuzzer.h
        external/SDL2/SDL_test_harness.h
        external/SDL2/SDL_test_images.h
        external/SDL2/SDL_test_log.h
        external/SDL2/SDL_test_md5.h
        external/SDL2/SDL_test_random.h
        external/SDL2/SDL_thread.h
        external/SDL2/SDL_timer.h
        external/SDL2/SDL_touch.h
        external/SDL2/SDL_types.h
        external/SDL2/SDL_version.h
        external/SDL2/SDL_video.h
        ministl/algo.cpp
        ministl/algo.h
        game_shared/voice_banmgr.cpp
        game_shared/voice_banmgr.h
        game_shared/voice_status.h
        game_shared/voice_gamemgr.cpp
        game_shared/voice_gamemgr.h
        pm_shared/pm_debug.cpp
        pm_shared/pm_debug.h
        pm_shared/pm_defs.h
        pm_shared/pm_info.h
        pm_shared/pm_materials.h
        pm_shared/pm_math.cpp
        pm_shared/pm_movevars.h
        pm_shared/pm_shared.cpp
        pm_shared/pm_shared.h)

target_include_directories(agmod PRIVATE
        ${CMAKE_BINARY_DIR}
        common
        dlls
        engine
        external
        external/discord-rpc/include
        game_shared
        pm_shared
        public
        utils/vgui/include)

if(MSVC)
    target_compile_options(agmod PRIVATE
            # Disable some warnings which would take too much effort to fix
            /wd4018 # Signed/unsigned mismatch
            /wd4838 # Conversion from double to float
            /wd4996 # The POSIX name for this item is deprecated
            )
else(MSVC)

    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -m32 -std=c++14 -shared")
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -m32 -std=c++14 -shared")
    set_target_properties(agmod PROPERTIES OUTPUT_NAME "ag.so")
    target_compile_options(agmod PRIVATE
            # High warning level and treat warnings as errors
            -Wall

            # Disable some warnings which would take too much effort to fix
            -Wno-parentheses
            -Wno-sign-compare
            -Wno-unused-function
            -Wno-unused-variable

            # Use the same FP instructions as others
            -march=pentium-m
            -mfpmath=387
            -mno-sse

            # Some additional flags from HLSDK
            -fno-strict-aliasing
            -fno-exceptions)

    # Some warnings are different between GCC and Clang
    if(CMAKE_CXX_COMPILER_ID MATCHES "Clang")
        target_compile_options(agmod PRIVATE
                -Wno-overloaded-virtual
                -Wno-unused-private-field
                -Wno-new-returns-null)
    else(CMAKE_CXX_COMPILER_ID MATCHES "Clang")
        target_compile_options(agmod PRIVATE
                -Wno-unused-but-set-variable
                -Wno-stringop-truncation
                -Wno-format-truncation
                -Wno-write-strings
                -Wno-unknown-pragmas

                $<$<COMPILE_LANGUAGE:CXX>:-Wno-class-memaccess>)
    endif(CMAKE_CXX_COMPILER_ID MATCHES "Clang")

    target_compile_definitions(agmod PRIVATE
            -DGNUC
            -DPOSIX
            -D_POSIX
            -DHL1
            -DCLIENT_WEAPONS
            -Dstricmp=strcasecmp
            -Dstrnicmp=strncasecmp
            -D_strnicmp=strncasecmp
            -D_snprintf=snprintf
            -D_snwprintf=swprintf
            -D_vsnprintf=vsnprintf
            -D_alloca=alloca)

    if(UNIX)
        target_compile_definitions(agmod PRIVATE
                -DLINUX
                -D_LINUX)
    endif(UNIX)
endif(MSVC)