cmake_minimum_required(VERSION 3.10)

project(libqueue LANGUAGES CXX)

add_library(queue INTERFACE)

target_include_directories(queue INTERFACE 
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

link_directories(queue INTERFACE linkedlist)