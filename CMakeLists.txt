cmake_minimum_required(VERSION 3.2)

project(project)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -O3")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(SOURCES main.cpp)

add_subdirectory(src)
add_subdirectory(test)

add_executable(project ${SOURCES})
