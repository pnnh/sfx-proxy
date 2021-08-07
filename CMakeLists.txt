cmake_minimum_required(VERSION 3.19)
project(sfxproxy)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_VERBOSE_MAKEFILE on)

include_directories(/usr/local/include)

add_executable(sfxproxy src/main.cpp)