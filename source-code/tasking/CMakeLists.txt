cmake_minimum_required(VERSION 3.16)
project(KokkosTutorialTasking)
include(../common.cmake)

if (Kokkos_ENABLE_CUDA)
    message(WARNING "CUDA is enabled, skipping tasking.")
    return()
elseif (DEFINED Kokkos_VERSION AND NOT Kokkos_VERSION VERSION_LESS 5.0.0)
    message(WARNING "Kokkos tasking was removed in Kokkos 5.0, skipping tasking.")
    return()
endif()

add_executable(fib.exe fib.cpp)
target_link_libraries(fib.exe Kokkos::kokkos)
