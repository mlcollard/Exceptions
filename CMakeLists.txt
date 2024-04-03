# @file CMakeLists.txt
# 
# CMake file for Exceptions

cmake_minimum_required(VERSION 3.28 FATAL_ERROR)

project(Exceptions)

# exceptions
add_executable(exceptions)
target_sources(exceptions PRIVATE Exceptions.cpp)
target_compile_features(exceptions PRIVATE cxx_std_17)
target_compile_options(exceptions PRIVATE
    $<$<CXX_COMPILER_ID:MSVC>:/Wall>
    $<$<CXX_COMPILER_ID:GNU,Clang,AppleClang>:-Wall>
)
