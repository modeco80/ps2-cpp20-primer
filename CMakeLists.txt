cmake_minimum_required(VERSION 3.19)

# Prohibit in-source tree builds.
# CMake will be banning this in a bit, so when we can adjust cmake_minimum_required
# to that exact CMake version, this block can be removed (or the policy enforced).
if(" ${CMAKE_SOURCE_DIR}" STREQUAL " ${CMAKE_BINARY_DIR}")
    message(FATAL_ERROR "In-source-tree builds are strictly prohibited. Please don't do them.")
endif()

include(${CMAKE_SOURCE_DIR}/cmake/Policies.cmake)
project(ps2-cpp20-primer LANGUAGES C CXX DESCRIPTION "C++20 Primer Project for the PlayStation 2.")

add_subdirectory(src/main)