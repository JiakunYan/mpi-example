cmake_minimum_required(VERSION 3.20)
project(mpi_example)

set(CMAKE_CXX_STANDARD 11)

find_package(MPI REQUIRED)

add_executable(main main.cpp)
#target_compile_options(main PRIVATE -target-accel=nvidia80)
target_link_libraries(main PRIVATE MPI::MPI_CXX)