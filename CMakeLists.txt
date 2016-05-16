project(game.libretro.beetle-psx)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(Kodi REQUIRED)
find_package(libretro-beetle-psx REQUIRED)

set(DEPLIBS beetle-psx)
set(BEETLE_PSX_CUSTOM_BINARY ${BEETLE_PSX_LIB}
                             ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} beetle-psx)

build_addon(${PROJECT_NAME} BEETLE_PSX DEPLIBS)
