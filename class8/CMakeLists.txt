cmake_minimum_required (VERSION 3.16)

project(Bowling)

include(cmake/CPM.cmake)

CPMAddPackage(
  NAME GTest
  GITHUB_REPOSITORY google/googletest
  GIT_TAG v1.16.0
  EXCLUDE_FROM_ALL ON
)
include(GoogleTest)

add_executable(bowling bowling.cxx)
target_link_libraries(bowling PRIVATE GTest::gtest_main)
gtest_discover_tests(bowling)
