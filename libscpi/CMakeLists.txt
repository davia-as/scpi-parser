cmake_minimum_required(VERSION 3.10)
project(libscpi)

# Add subdirectories
add_subdirectory(inc)
add_subdirectory(src)

# Define the library with sources gathered from subdirectories
add_library(libscpi STATIC ${LIB_SOURCES})

# Set include directories for the library (from inc/CMakeLists.txt)
target_include_directories(libscpi PUBLIC ${LIB_INCLUDES})