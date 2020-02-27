# Set the verison
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

# Name and supported languages
project("Example" C)

# Enable Debug symbols
set(CMAKE_BUILD_TYPE Debug)

# Set the compilation standard like with gcc
# e.g. gcc -std=c99
# -fdump-rtl-expand creates extra output files that you can pass to Egypt to
# create code graphs.
set(CMAKE_C_FLAGS "-std=c99 -fdump-rtl-expand")

# CMake expects a CMakeLists.txt file in directory src
add_subdirectory(src)
# Placing Unity in lib in case we ever want to add more libraries
add_subdirectory(lib)
add_subdirectory(test)
