cmake_minimum_required(VERSION 3.20.0)
project(TOOLKIT)

add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/deps/Mapping")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/modules/module1/")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/modules/module2/")
