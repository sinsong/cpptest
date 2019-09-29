cmake_minimum_required(VERSION 3.2)

project(CPPTEST
VERSION 0.0.1
DESCRIPTION "a test program"
LANGUAGES CXX
)

option(ENABLE_COVERAGE "Enable source base coverage" OFF)

if(ENABLE_COVERAGE)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fprofile-instr-generate='${PROJECT_BINARY_DIR}/default.profraw' -fcoverage-mapping")
endif()

add_subdirectory(src)

message("[PROJECT_SOURCE_DIR]" ${PROJECT_SOURCE_DIR})
message("[PROJECT_BINARY_DIR]" ${PROJECT_BINARY_DIR})