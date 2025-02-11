cmake_minimum_required(VERSION 3.16)

project(hello LANGUAGES C CXX)

add_library(stuff greeting.cxx factorial.cxx hello.h)

add_executable(hello hello.cxx)
target_link_libraries(hello PRIVATE stuff)

add_subdirectory(bowling)
