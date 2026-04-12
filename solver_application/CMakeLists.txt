cmake_minimum_required(VERSION 3.10)

project(solver)

add_subdirectory(../solver_lib solver_lib_build)
add_subdirectory(../formatter_ex_lib formatter_ex_lib_build)

add_executable(equation equation.cpp)

target_link_libraries(equation PRIVATE solver formatter_ex)
