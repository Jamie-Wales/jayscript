cmake_minimum_required(VERSION 3.10)
project(vm)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

include_directories(include)

file(GLOB_RECURSE SOURCES "src/*.cpp")

add_executable(vm ${SOURCES}
        src/Compiler.cpp)

add_compile_options(-Wall -Wextra -Wpedantic)
