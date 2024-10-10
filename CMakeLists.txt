cmake_minimum_required(VERSION 3.2)

project(project)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -O3")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(SOURCES main.cpp)

include_dicertories(${PATH_TO_DIRS})

add_subdirectory(src)
add_subdirectory(test)

add_library(project SHARED/STATIC ${SOURCES})
add_executable(project ${SOURCES})

target_link_libraries(project ${LIBS})
