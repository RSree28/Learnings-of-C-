cmake_minimum_required(VERSION 3.14)

project(example LANGUAGES CXX)

add_executable(hello hello.cpp)

add_library(greeting
  SHARED
    greeting.cpp
    greeting.hpp
  )

target_link_libraries(hello PRIVATE greeting)

include(CMakePrintHelpers)

cmake_print_variables(CMAKE_CXX_COMPILER_ID)
cmake_print_variables(CMAKE_CXX_COMPILER_VERSION)
cmake_print_variables(SOMETHING_UNDEFINED)
