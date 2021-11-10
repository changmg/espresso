# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.16)

# Set the project name
project(espresso)

# Collect source files
aux_source_directory(${PROJECT_SOURCE_DIR}/src sources)

# Add definitions
add_definitions(-g -Wall -O3)

# Add an static library with the above sources
add_library(${PROJECT_NAME} STATIC ${sources})

# Add include paths
target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR}/espresso/src)
