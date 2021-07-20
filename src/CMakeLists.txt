project(sf2repo)
cmake_minimum_required(VERSION 2.4)

include(FindPkgConfig)
pkg_check_modules(GIG gig)
pkg_check_modules(SNDFILE sndfile)

if(SNDFILE_FOUND)
    add_compile_options("-DHAVE_SNDFILE")
endif()

INCLUDE_DIRECTORIES(${GIG_INCLUDE_DIRS})

add_executable (sf2dump sf2dump.cpp helper.cpp)
target_link_libraries (sf2dump LINK_PUBLIC gig)

add_executable (sf2extract sf2extract.cpp helper.cpp)
target_link_libraries (sf2extract LINK_PUBLIC gig sndfile)


