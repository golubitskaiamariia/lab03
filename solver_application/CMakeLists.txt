cmake_minimum_required(VERSION 3.5)
project(solver_app)

add_executable(solver_app equation.cpp)
target_include_directories(solver_app PRIVATE
    ${CMAKE_SOURCE_DIR}/formatter_ex_lib
    ${CMAKE_SOURCE_DIR}/formatter_lib
    ${CMAKE_SOURCE_DIR}/solver_lib
)

target_link_libraries(solver_app PRIVATE formatter_ex solver_lib)
