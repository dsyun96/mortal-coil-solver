cmake_minimum_required(VERSION 3.30)
project(mortal_coil_solver)

set(CMAKE_CXX_STANDARD 20)

MATH(EXPR stack_size "128 * 1024 * 1024") # 128MB
set(CMAKE_EXE_LINKER_FLAGS "-Wl,--stack,${stack_size}")

add_executable(mortal_coil_solver main.cpp)
