cmake_minimum_required(VERSION 3.12)

project(armneon LANGUAGES CXX)

set(CMAKE_CXX_COMPILER "/usr/bin/aarch64-linux-gnu-g++")
set(CMAKE_CXX_FLAGES "${CMAKE_CXX_FLAGES} -std=c++11")
add_definitions("-Wall -g")

find_package(OpenCV REQUIRED)
message("OpenCV version : ${OpenCV_VERSION}")
#set(OpenCV_INCLUDE_DIRS ${PROJECT_SOURCE_DIR}/inlude/opencv2.4.9/opencv2)
#set(OpenCV_LIB_DIR ${PROJECT_SOURCE_DIR}/library/opencv2.4.9/)

include_directories(${OpenCV_INCLUDE_DIRS})
link_directories(${OpenCV_LIB_DIRS})

#message("OpenCV lib dir : ${OpenCV_LIB_DIR}")
#message("OpenCV include dir : ${OpenCV_INCLUDE_DIRS}")

add_executable(unit_test ${PROJECT_SOURCE_DIR}/src/unit_test.cpp)

target_link_libraries(unit_test ${OpenCV_LIBS})
