cmake_minimum_required(VERSION 3.1)
project(LabM)

#Fedora find mpi workaround
set(CMAKE_PREFIX_PATH /usr/lib64/mpich)

find_package(MPI REQUIRED)

message(STATUS MPI_CXX_COMPILER ${MPI_CXX_COMPILER})
message(STATUS MPI_CXX_INCLUDE_PATH ${MPI_CXX_INCLUDE_PATH})
message(STATUS MPI_CXX_COMPILE_FLAGS ${MPI_CXX_COMPILE_FLAGS})
message(STATUS MPI_CXX_LINK_FLAGS ${MPI_CXX_LINK_FLAGS})

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_VERBOSE_MAKEFILE ON)

include_directories(${MPI_CXX_INCLUDE_PATH})
include_directories(Utils)

add_subdirectory(LabM1)
add_subdirectory(LabM2)
add_subdirectory(LabM3)
add_subdirectory(LabM4)
