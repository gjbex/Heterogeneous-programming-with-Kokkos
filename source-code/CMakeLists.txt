cmake_minimum_required(VERSION 3.22)

project(kokkos LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

include(FetchContent)
FetchContent_Declare(
  kokkos
  GIT_REPOSITORY https://github.com/kokkos/kokkos.git
  GIT_TAG        5.1.0
)
FetchContent_MakeAvailable(Kokkos)

file(GLOB src_files  "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")
foreach(src_file ${src_files})
    get_filename_component(base_name ${src_file} NAME_WE)
    set(executable_name "${base_name}.exe")
    add_executable(${executable_name} ${src_file})
    target_include_directories(${executable_name} PRIVATE Kokkos::kokkos)
    target_link_libraries(${executable_name} Kokkos::kokkos)
    target_compile_options(${executable_name} PRIVATE -Wall -Wextra -pedantic)
endforeach()

add_subdirectory(gemv)
add_subdirectory(gemm)
add_subdirectory(scratch)
add_subdirectory(multiple_exec_spaces)
add_subdirectory(random_walks)
if (Kokkos_ENABLE_CUDA)
    add_subdirectory(cuda_required)
else()
    message(WARNING "CUDA is not enabled, skipping cuda_required.")
endif()
