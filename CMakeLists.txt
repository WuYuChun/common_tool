cmake_minimum_required(VERSION 2.8.0)
project(common_tool)

find_package(CUDA REQUIRED)

if(NOT DEFINED CMAKE_CUDA_STANDARD)
    set(CMAKE_CUDA_STANDARD 11)
    set(CMAKE_CUDA_STANDARD_REQUIRED ON)
endif()

include_directories(include)

add_library(common_tool SHARED src/timer.cpp)