cmake_minimum_required(VERSION 3.12)

project(armneon LANGUAGES CXX)

#set(CMAKE_CXX_COMPILER "/usr/bin/aarch64-linux-gnu-g++")
#set(CMAKE_CXX_FLAGES "${CMAKE_CXX_FLAGES} -std=c++11")
#add_definitions("-Wall -g")

#find_package(OpenCV REQUIRED)
#message("OpenCV version : ${OpenCV_VERSION}")
#set(OpenCV_INCLUDE_DIRS ${PROJECT_SOURCE_DIR}/opencv/include/opencv ${PROJECT_SOURCE_DIR}/opencv/include/opencv2)
#set(OpenCV_LIB_DIR ${PROJECT_SOURCE_DIR}/opencv/library)

#target_include_directories(${OpenCV_INCLUDE_DIRS})
#link_directories(${OpenCV_LIB_DIR})

#message("OpenCV lib dir : ${OpenCV_LIB_DIR}")
#message("OpenCV include dir : ${OpenCV_INCLUDE_DIRS}")

add_subdirectory(src)
add_subdirectory(unit_test)