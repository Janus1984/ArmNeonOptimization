project(unit_test)

find_package(OpenCV REQUIRED)
add_executable(unit_test unit_test.cpp)

if(OpenCV_FOUND)
    message(${OpenCV_VERSION})
    target_include_directories(unit_test PUBLIC ${OpenCV_INCLUDE_DIRS})
    target_link_libraries(unit_test PUBLIC ${OpenCV_LIBS})
    
endif(OpenCV_FOUND)

target_include_directories(unit_test PUBLIC ../include)
target_link_libraries(unit_test PUBLIC src)
