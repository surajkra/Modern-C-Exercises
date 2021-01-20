# Specify the minimum version for CMake

cmake_minimum_required(VERSION 2.8)

# Project's name

project(test_main)

# Set the output folder where your program will be created

set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# The following folder will be included
include_directories("${PROJECT_SOURCE_DIR}")

# add_executable(test_main ${PROJECT_SOURCE_DIR}/main.cpp ${PROJECT_SOURCE_DIR}/test.cpp)
add_executable(toDo ${PROJECT_SOURCE_DIR}/main.cpp 
                    ${PROJECT_SOURCE_DIR}/ToDo.cpp)

