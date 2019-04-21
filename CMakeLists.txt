cmake_minimum_required(VERSION 3.2)

project(CPPTEST
VERSION 0.0.1
DESCRIPTION "a test program"
LANGUAGE CXX
)

add_subdirectory(src)

message("[PROJECT_SOURCE_DIR]" ${PROJECT_SOURCE_DIR})
message("[PROJECT_BINARY_DIR]" ${PROJECT_BINARY_DIR})