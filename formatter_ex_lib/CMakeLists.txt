cmake_minimum_required(VERSION 3.5)

project(formatter_ex)

include_directories(${CMAKE_SOURCE_DIR}/../formatter_lib)

add_subdirectory(../formatter_lib ${CMAKE_BINARY_DIR}/formatter_lib)

add_library(formatter_ex STATIC formatter_ex.cpp)
target_link_libraries(formatter_ex PRIVATE formatter)
