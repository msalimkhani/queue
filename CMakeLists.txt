cmake_minimum_required(VERSION 3.10)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(libqueue LANGUAGES CXX)

add_subdirectory(linkedlist)

add_library(queue INTERFACE)

target_include_directories(queue INTERFACE 
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_link_libraries(queue INTERFACE linkedlist)