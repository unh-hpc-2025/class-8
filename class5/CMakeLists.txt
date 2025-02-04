cmake_minimum_required (VERSION 3.16)

project(hello LANGUAGES C)

add_executable(hello hello.c greeting.c factorial.c)