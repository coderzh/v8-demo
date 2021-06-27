cmake_minimum_required(VERSION 2.8)
project (v8_demo)

set(CMAKE_EXPORT_COMPILE_COMMANDS "YES")
set(CMAKE_CXX_STANDARD 14)

add_definitions(-DV8_COMPRESS_POINTERS)
link_directories(${CMAKE_SOURCE_DIR}/libs)
include_directories(include)

add_executable(v8_demo src/main.cc)

target_link_libraries(v8_demo v8_monolith)
