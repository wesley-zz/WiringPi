cmake_minimum_required(VERSION 3.10)

set(PROJECT_NAME mark_1)
project(${PROJECT_NAME} VERSION 1.0.0)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS True)

include_directories(${PROJECT_SOURCE_DIR}/wiringPi)
aux_source_directory(${PROJECT_SOURCE_DIR}/wiringPi wiringPi_SRCS)
# message(STATUS "wiringPi_SRCS = " ${wiringPi_SRCS})
add_library(wiringPi ${wiringPi_SRCS})
add_definitions("-Wall -g")