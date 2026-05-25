cmake_minimum_required(VERSION 3.10)

project(lab05)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-error=maybe-uninitialized")

option(BUILD_TESTS "Build tests" ON)

add_subdirectory(banking)

if(BUILD_TESTS)
    enable_testing()

    add_subdirectory(third-party/gtest)
    add_subdirectory(tests)
endif()
