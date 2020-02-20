# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.10)

project ("CMakeDynamicLib")

set(TRY_INSTALL_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)

include_directories(${TRY_INSTALL_INCLUDE_DIR})

# Include sub-projects.
add_subdirectory ("src")
