cmake_minimum_required(VERSION 2.6)
project(HelloCMake)

if(NOT ${CMAKE_TOOLCHAIN_FILE} STREQUAL "")
    get_filename_component(TOOLCHAIN_FILE_NAME ${CMAKE_TOOLCHAIN_FILE} NAME)
    if(TOOLCHAIN_FILE_NAME STREQUAL "Emscripten.cmake")
        set(CMAKE_EXECUTABLE_SUFFIX ".html")
    endif()
endif()

add_executable(HelloCMake main.c)
