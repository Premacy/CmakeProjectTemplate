cmake_minimum_required(VERSION 3.2)

set(PROJECT_NAME TestProject)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -O3")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(SOURCES main.cpp)

set(PATH_TO_DIRS ${CMAKE_SOURCE_DIR})
include_directories(${PATH_TO_DIRS})

add_subdirectory(src)
add_subdirectory(test)

add_library(${PROJECT_NAME} SHARED/STATIC ${SOURCES})
add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} ${LIBS})
