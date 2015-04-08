cmake_minimum_required(VERSION 3.1)

project(Symlinks)

set (Symlinks_VERSION_MAJOR 1)
set (Symlinks_VERSION_MINOR 5)

# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/cmake_configuration.h.in"
  "${PROJECT_BINARY_DIR}/cmake_configuration.h"
  )

# add the binary tree to the search path for include files
include_directories("${PROJECT_BINARY_DIR}")

set(SOURCE_FILES
    symlinks.c)

add_executable(Symlinks ${SOURCE_FILES})