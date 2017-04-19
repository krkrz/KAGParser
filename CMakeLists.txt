
cmake_minimum_required(VERSION 3.4.1)

set( CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS}-Wl,--version-script=${CMAKE_CURRENT_SOURCE_DIR}/version_script.map -Wl,--strip-debug -Wl,--discard-all" )

include_directories( ./
             ../)

add_library( kagparser

             SHARED

             Main.cpp
             KAGParser.cpp
             ../tp_stub.cpp)

target_link_libraries( kagparser )

