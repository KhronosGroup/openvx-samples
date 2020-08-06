cmake_minimum_required(VERSION 3.10.2)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the type of build, options are: Debug, Release, or MinSizeRel." FORCE)
    message(STATUS "CMAKE_BUILD_TYPE not set, defaulting to Release.")
endif()

project(openvx-samples LANGUAGES CXX)

add_subdirectory(bubble-pop)
add_subdirectory(canny-edge-detector)
add_subdirectory(skin-tone-detector)
