project(src)

set(SRC boxFilter.cpp)
add_library(src STATIC ${SRC})

target_include_directories(src PUBLIC ../include)
