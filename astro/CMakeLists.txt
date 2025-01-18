cmake_minimum_required(VERSION 3.28)
project(astro)

set(CMAKE_CXX_STANDARD 17)

add_executable(astro main.cpp
        Game.cpp
        Game.h)

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake_modules)

set(SDL2_PATH "C:/Users/dj8ch/Downloads/SDL2-devel-2.30.11-mingw/SDL2-2.30.11/x86_64-w64-mingw32")

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIR})

target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARY})

