cmake_minimum_required(VERSION 3.17)
set(CMAKE_CXX_STANDARD 20)

set(SOURCE_FILES
        insertionsort.h
        insertionsort.cpp
        quicksort.cpp
        quicksort.h)


add_library(core ${SOURCE_FILES})
add_executable(executable
        source.cpp
        ${SOURCE_FILES})

install(TARGETS core DESTINATION lib EXPORT core) 
